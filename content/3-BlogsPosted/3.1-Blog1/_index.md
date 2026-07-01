---
title: "Blog 1"
date: 2026-07-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Building Reliable Multi-Step Workflows with AWS Lambda Durable Functions

Modern applications often need to process multi-step sequential workflows – such as order processing, user onboarding, or coordinating AI workflows that make multiple calls to Large Language Models (LLMs) and external tools. In the past, to implement this on AWS Lambda, developers had to stitch together Step Functions, SQS, and DynamoDB to store state, resulting in complex infrastructure.

At re:Invent 2025, AWS introduced **AWS Lambda Durable Functions** – allowing you to write the entire workflow as sequential code inside a single Lambda function, while retaining fault tolerance and long-term pausing capabilities.

### What is AWS Lambda Durable Functions?

Durable Functions are regular Lambda functions enabled with "durable execution" mode. This feature extends Lambda's programming model with two new primitives: “steps” and “waits”, allowing automatic checkpointing, error recovery, and pausing execution for up to one year without incurring compute costs while waiting. You don't need to manage additional infrastructure or write custom code for state management and error handling.

Technically, it works using a checkpoint and replay mechanism: when an error occurs, Lambda reruns the function from the beginning but skips completed steps (which have checkpoints) and reuses their saved results, preserving progress.

### Limitations of Traditional Lambda

With standard Lambda, your code runs from start to finish in a single invocation and is completely stateless. This creates three major limitations when building complex workflows:
1. **State loss on failure:** If an error occurs at any step, the entire function must be retried from the beginning; all state must be manually saved to DynamoDB or S3.
2. **Execution time limit:** A single execution is capped at 15 minutes, which is unsuitable for long-running workflows or those requiring human approval.
3. **Manual idempotency management:** Developers must protect against duplicate invocations and build safe deployment strategies manually.

### How It Works: Checkpoint & Replay

Durable Functions resolve these issues using two core primitives in the open-source Durable Execution SDK:
- **Step – `context.step()`:** Wraps a block of business logic to automatically checkpoint and retry. Once a step completes, it is skipped in the next replay.
- **Wait – `context.wait()` / callback:** Pauses execution for a duration or until an external signal is received (e.g., human approval). While waiting, the function is terminated, incurring no compute costs, and automatically resumes later.

The architecture diagram below illustrates an AI workflow using Durable Functions: a client calls via API Gateway to a Lambda function (with durable execution enabled); the function uses `step()` to call Bedrock (LLM) and saves the result to DynamoDB – each step is checkpointed automatically; it uses `wait()`/`callback` to pause for human approval and then resumes; execution state is emitted to EventBridge and CloudWatch for monitoring:

![AI workflow architecture with AWS Lambda Durable Functions](/images/3-Blog/3.1-Blog1/durable-functions-arch.png)
*Figure 1: AI workflow architecture with AWS Lambda Durable Functions (step, wait/callback, checkpoint).*

### Key Highlights & Core Benefits

- **Automatic fault tolerance:** The SDK automatically checkpoints, retries with configurable backoff, and ensures idempotency (only one execution runs per request even if upstream calls again).
- **Pause for up to one year:** Perfect for human-in-the-loop workflows, approval gates, or scheduled processing – no compute cost during pause.
- **Familiar Lambda experience:** It remains a Lambda function with the same event handler and integration; you just toggle a "durable execution" switch when creating the function.
- **Multi-language support:** The SDK supports JavaScript, TypeScript, Python, and Java (Java is in Developer Preview, compatible with Java 17+).

### Ideal Use Cases

- **Multi-step AI workflows:** Orchestrating LLM call chains, tool calling, and result processing safely even if a single call fails.
- **Order processing & payments:** Maintaining transaction state across failures, retrying automatically, and orchestrating authorization, fraud checks, and settlement across multiple providers.
- **Human-in-the-loop approvals:** Document approval, leave request processes – pausing for human decisions before continuing.
- **Long-running / scheduled tasks:** Multi-day onboarding, trial subscriptions, delayed notifications, batch processing within time windows.

### Code Example (Python)

After enabling durable execution and adding the SDK, you use `DurableContext` to wrap each business step. The core concepts lie in `context.step()` and `context.wait()`:

```python
def handler(event, context):
    # Step 1: call LLM - automatically checkpointed
    summary = context.step("summarize", lambda: call_llm(event))

    # Step 2: wait for human approval (free compute while waiting)
    decision = context.wait_for_callback("approval")

    # Step 3: only runs if approved - skips completed steps during replay
    if decision == "approved":
        context.step("persist", lambda: save_result(summary))
```
*Note:* Although the overall workflow can last up to a year, each Lambda container still runs for a maximum of 15 minutes between checkpoints/waits.

### Release Status

Lambda Durable Functions was announced on December 2, 2025 (re:Invent 2025), generally available (GA) initially in US East (Ohio) with Python (3.13, 3.14) and Node.js (22, 24) runtimes, expanding to more regions. Can be enabled via Console, AWS CLI, SAM, CloudFormation, CDK, or SDK. The Java SDK launched in Developer Preview on February 26, 2026.

### Conclusion

AWS Lambda Durable Functions bridge the gap between Lambda's simplicity and complex workflow orchestrators. Instead of stitching together Step Functions, SQS, and DynamoDB, you write sequential logic in a single function and let the SDK handle checkpointing, retries, and pausing. It is ideal for multi-step AI workflows, order processing, and human approval gates.

### References

1. [Build multi-step applications and AI workflows with AWS Lambda durable functions](https://aws.amazon.com/blogs/compute/build-multi-step-applications-and-ai-workflows-with-aws-lambda-durable-functions/) (AWS News Blog)
2. [Building fault-tolerant applications with AWS Lambda durable functions](https://aws.amazon.com/blogs/compute/building-fault-tolerant-applications-with-aws-lambda-durable-functions/) (AWS Compute Blog)
3. [AWS Lambda durable functions – Product page](https://aws.amazon.com/lambda/features/durable-functions/)
4. [AWS Lambda announces durable functions for multi-step applications and AI workflows](https://aws.amazon.com/about-aws/whats-new/2025/12/aws-lambda-durable-functions-multi-step-applications-ai-workflows/) (What's New)
5. [Durable execution SDK – AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/durable-execution-sdk.html)
