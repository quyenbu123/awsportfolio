---
title: "Blog 2"
date: 2026-07-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Next-Gen OpenSearch Serverless: Vector Search Scale-to-Zero for AI Agent Applications

AI agent applications have a very unique traffic profile: an agent might fire hundreds of vector queries while reasoning through a task, and then stay quiet for hours. With traditional search infrastructure, you still pay for idle capacity during those quiet times.

On May 28, 2026, AWS announced the next generation of **Amazon OpenSearch Serverless** (referred to as **NextGen**) – a search and vector engine redesigned from the ground up to serve exactly this type of unpredictable workload.

### What is OpenSearch Serverless NextGen?

NextGen is the new architecture of Amazon OpenSearch Serverless, a fully managed search and vector engine. The core aspect is that it completely decouples compute and storage through a shared storage layer, allowing compute capacity to scale independently of the volume of data stored. As a result, the service can provision resources in seconds and scale down to zero when the application is idle.

AWS names two architectures: old collections are now called **Classic**, while the new architecture is **NextGen** and is the default when creating new collections via the Console. In the API/CLI, you specify `--generation NEXTGEN` (or `--generation CLASSIC` to keep the old architecture).

### Limitations of the Classic Architecture

The initial Serverless architecture always maintained a minimum of two OpenSearch Compute Units (OCUs) running continuously. While this made sense for a production search engine with stable load, it is wasteful for agentic workloads:
1. **Pay even when idle:** Compute is always provisioned at a minimum level, so you incur costs even with zero queries.
2. **Compute bound to storage:** You cannot scale compute independently of stored data volume.
3. **Slow scaling:** Provisioning resources takes minutes, making it hard to keep up with sudden traffic spikes from agentic workflows.

### How NextGen Works: Decoupled Compute & Storage

The foundational change in NextGen is decoupling compute from storage. A new shared storage layer is accessed by both indexing OCUs and search OCUs, meaning OCUs can scale up and down regardless of the volume of data stored. You can have many indexes containing data without incurring compute costs unless you are actively indexing or searching.

The architecture diagram below illustrates how NextGen serves an AI agent: the agent creates embeddings via Bedrock and writes them to the Indexing OCU; vector queries pass through the Search OCU. Both Indexing and Search OCUs (the compute layer) scale independently and share a decoupled Shared Storage Layer, enabling scale-to-zero when idle:

![Amazon OpenSearch Serverless NextGen Architecture](/images/3-Blog/3.2-Blog2/opensearch-nextgen-arch.png)
*Figure 1: Amazon OpenSearch Serverless NextGen Architecture – compute (OCU) decoupled from shared storage.*

### Key Highlights & Core Benefits

- **True scale-to-zero:** When there are no requests during the idle window (10 minutes), the service releases compute and OCUs go to 0 – stopping compute billing. When traffic returns, capacity is restored within approximately 10 seconds.
- **20x faster scaling:** Provisions resources in seconds and scales capacity up to 20 times faster than the previous generation, satisfying even the most unpredictable agentic workflows.
- **Up to 60% cost savings:** For workloads with significant idle time, the new architecture reduces infrastructure costs by up to 60% compared to provisioning clusters for peak load.
- **AI-native integration:** Built-in integrations with AI development platforms like Vercel and Kiro; part of OpenSearch Agent Skills to be used directly in Claude Code, Cursor, and Codex using natural language commands.

### Ideal Use Cases

- **Vector backend for AI agents:** Storing and querying vector embeddings for RAG and semantic search while paying only when the agent actually queries.
- **Semantic Search:** Maintaining vector indexes for natural language queries without managing a separate Vector Database.
- **Unpredictable workloads:** E.g., e-commerce sites scaling 10x during flash sales and then returning to zero – scaling instantly without pre-provisioning for peak load.
- **Dev/Test environments:** Express Create builds a collection quickly with default policies, ideal for testing (production should configure explicit encryption, network, and data access policies).

### Release Status

The next generation of OpenSearch Serverless was announced on May 28, 2026, and is generally available (GA). At launch, two types of collections are supported: full-text search and vector search. Collections can be created via the Console, AWS SDK, and AWS CLI; CloudFormation support is coming soon. 

*Note:* 'shared storage' is still billed per GB-month even when compute is scaled to zero, so the 20x and 60% figures are conditional, tied to a specific baseline and workloads with substantial idle time.

### Conclusion

OpenSearch Serverless NextGen solves the cost equation for the AI agent era: traffic bursts followed by silence. By decoupling compute and storage to scale to zero, it enables production-ready search and vector backends in minutes, billing based on actual usage. It is a natural fit for RAG and semantic search architectures without the overhead of operating a separate Vector Database.

### References

1. [Introducing the next generation of Amazon OpenSearch Serverless for building your agentic AI applications](https://aws.amazon.com/blogs/database/introducing-the-next-generation-of-amazon-opensearch-serverless-for-building-your-agentic-ai-applications/) (AWS News Blog)
2. [The next generation of Amazon OpenSearch Serverless: Built from the ground up for agents](https://aws.amazon.com/blogs/big-data/the-next-generation-of-amazon-opensearch-serverless-built-from-the-ground-up-for-agents/) (AWS Big Data Blog)
3. [The next generation of Amazon OpenSearch Serverless is now generally available](https://aws.amazon.com/about-aws/whats-new/2026/05/next-generation-amazon-opensearch-serverless-generally-available/) (What's New)
4. [Amazon OpenSearch Service Pricing](https://aws.amazon.com/opensearch-service/pricing/)
