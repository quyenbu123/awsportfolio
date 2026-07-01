---
title: "Workshop"
date: 2026-06-29
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

Hands-on workshop to set up the cloud infrastructure and secure S3 connection for the Money Manager project:

### [5.1. Introduction](5.1-workshop-overview/)
General introduction of the technical workshop dedicated to building and validating the cloud infrastructure for the Money Manager platform aligned with AWS Well-Architected.

### [5.2. Prerequisites](5.2-prerequiste/)
Prerequisite setup instructions covering AWS Account management, IAM Access Key credentials for CLI, local terminal environment installations (Node.js, JDK, Maven, Docker), and Singapore region targeting.

### [5.3. Detailed Implementation Steps](5.3-implementation-steps/)
Step-by-step walkthrough of 4 core phases: constructing VPC network topology & EC2 hosts; configuring RDS MySQL & ElastiCache Redis; integrating DynamoDB & AWS SQS; and configuring S3 Security & VPC Endpoints.

### [5.4. Validation & Performance Analysis](5.4-validation/)
Validation procedures covering private DNS resolution, S3 bucket access restrictions, DynamoDB/SQS integration, along with data latency and NAT Gateway cost savings analysis.

### [5.5. Resource Cleanup](5.5-cleanup/)
Standard cleanup steps (S3 objects deletion, detaching/deleting VPC Endpoints, resetting Route 53 Resolver, EC2 Docker system prune) to prevent recurring AWS billing.