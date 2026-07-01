---
title: "Validation & Performance Analysis"
date: 2026-07-01
weight: 4
chapter: false
pre: " <b> 5.4. </b> "
---

We conducted practical testing procedures to validate the integrity and performance of the deployed cloud architecture:

### DNS Routing Verification
Running DNS lookup tools inside the EC2 API server container targets the S3 public domain name. The query resolves directly to the Private IP addresses of the Interface Endpoint ENIs instead of S3 public IPs, confirming private routing and DNS mappings are active.

![Money Manager web application successfully loaded at botdevgroup.me, verifying DNS routing works seamlessly](/images/5-Workshop/5.4-Validation/dns-routing-site-loaded.png?width=60pc&classes=shadow)

### S3 Storage Access Verification
Uploading invoice images from the EC2 instance succeeds via the SDK Client. When a personal workstation outside the AWS network attempts to access the S3 bucket (even when utilizing Admin IAM credentials), AWS rejects the request with a 403 Access Denied error, validating that the S3 Bucket Policy restricts external access.

![Notification on the dashboard confirming that the monthly report was generated and exported successfully](/images/5-Workshop/5.4-Validation/s3-export-notification.png?width=60pc&classes=shadow)

![Contents of the exported report file, confirming S3 upload/download flows are correct](/images/5-Workshop/5.4-Validation/s3-exported-report-content.png?width=40pc&classes=shadow)

### DynamoDB & SQS Integration Verification
Nova Money chat records are successfully written to both DynamoDB tables. Transaction events sent to SQS are pulled and processed by the Worker container instantly, leaving no pending messages in SQS or DLQ queues.

![A test conversation with the Nova Money AI assistant used to generate chat data](/images/5-Workshop/5.4-Validation/nova-money-chat-test.png?width=60pc&classes=shadow)

![Scanning the chat_messages table on AWS Console confirms the test conversation is correctly stored](/images/5-Workshop/5.4-Validation/dynamodb-chat-messages-scan.png?width=60pc&classes=shadow)

### Performance & Cost Impact Analysis
* **Latency:** Routing traffic privately reduces file upload latency to S3 from an average of 180ms to only **45ms**.
* **Cost:** Crucially, S3 data transfers via the NAT Gateway drop to **$0**, eliminating all associated NAT Gateway data processing charges on the AWS cloud environment.
