---
title: "Week 8 Worklog - AWS Well-Architected & Money Manager Architecture Design"
date: 2026-04-17
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Weekly Focus

Learning AWS Well-Architected Framework, AWS SAM and applying them to design the Money Manager architecture

### Objectives

* Understand the 5 pillars of the AWS Well-Architected Framework.
* Design the AWS architecture for Money Manager based on best practices.

### Work Schedule

| Date | Day | Work Items | Lab / Project |
|---|---|---|---|
| 08/06/2026 | Monday | Study the AWS Well-Architected Framework and its 5 pillars.Hands-on with AWS SAM — deploy a simple serverless app.Start drafting the AWS architecture for Money Manager (VPC, EC2, RDS, ElastiCache). | Well-Architected Labs |
| 09/06/2026 | Tuesday | Dive deeper into Well-Architected principles and real-world trade-offs.Continue AWS SAM practice with a serverless deploy flow.Design the VPC layout: Public Subnet (ALB, NAT Gateway), Private Subnet (EC2, RDS, ElastiCache). | Well-Architected Labs |
| 10/06/2026 | Wednesday | Review design decisions through the lens of all 5 pillars.Explore more AWS SAM patterns for serverless deployment.Design the async flow: SQS -> EC2 Worker -> Lambda -> S3 for report generation and invoice rendering. | Well-Architected Labs |
| 11/06/2026 | Thursday | Evaluate Reliability, Security and Cost Optimization in the Money Manager architecture.Practice packaging and deploying serverless apps with AWS SAM.Design the AI chat flow: DynamoDB for storing Nova Money conversation history. | Well-Architected Labs |
| 12/06/2026 | Friday | Consolidate the 5 pillars and their impact on the Money Manager architecture.Complete the basic AWS SAM hands-on exercises.Finalize the proposed architecture: multi-AZ, ALB + EC2 ASG, RDS MySQL, ElastiCache HA, SQS + Lambda. | Well-Architected Labs |

### Expected Outcomes

* Understand the 5 pillars of AWS Well-Architected Framework and how to apply them.
* Hands-on experience with AWS SAM.
* Finalized AWS architecture for Money Manager: VPC multi-AZ, ALB, EC2 ASG, RDS MySQL, ElastiCache, DynamoDB, SQS, Lambda, S3, SNS, CloudWatch.

### Week 8 References

* Well-Architected Labs
* 5 Pillars: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization
