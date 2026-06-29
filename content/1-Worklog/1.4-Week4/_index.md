---
title: "Week 4 Worklog - Auto Scaling, Route 53, DynamoDB, CloudFront & HA Architecture"
date: 2026-04-17
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Weekly Focus

Auto Scaling + Route 53 + DynamoDB + CloudFront + highly available architecture

### Objectives

* Learn EC2 Auto Scaling, Application Load Balancer, Route 53 DNS, DynamoDB, CloudFront, and Highly Available architecture.

### Work Schedule

| Date | Day | Work Items | Lab / Project |
|---|---|---|---|
| 11/05/2026 | Monday | Create a launch template and Auto Scaling Group.Configure a target tracking scaling policy.Set up an Application Load Balancer with listener rules.Test scale-out, scale-in, and health check behavior in Lab 000006. | Lab 000006 - Scaling Apps with EC2 Auto Scaling |
| 12/05/2026 | Tuesday | Learn Route 53 hosted zones and common record types such as A, CNAME, and Alias.Configure basic routing policies.Set up a hybrid DNS pattern with VPC integration.Practice Lab 000010. | Lab 000010 - Hybrid DNS Management with Amazon Route 53 |
| 13/05/2026 | Wednesday | Create a DynamoDB table with partition key and sort key design.Perform CRUD operations through the console and CLI.Configure a Global Secondary Index and compare on-demand versus provisioned capacity.Practice Lab 000060 and clean up resources. | Lab 000060 - NoSQL Database Essentials with Amazon DynamoDB |
| 14/05/2026 | Thursday | Learn CloudFront fundamentals including distributions, origins, and cache behaviors.Integrate CloudFront with an S3 static website.Configure HTTPS with ACM and perform cache invalidation.Practice Lab 000094. | Lab 000094 - Content Delivery with CloudFront |
| 15/05/2026 | Friday | Design a Multi-AZ architecture using ALB, EC2, and RDS.Configure target groups and listener rules.Deploy RDS Multi-AZ and test health checks plus failover behavior.Practice Lab 000101. | Lab 000101 - Building Highly Available Web Apps |

### Expected Outcomes

* Understand how EC2 Auto Scaling, ALB, and scaling policies work together in an elastic architecture.
* Configure Route 53 DNS records and basic routing strategies, including hybrid DNS concepts.
* Work with DynamoDB table design, CRUD operations, secondary indexes, and capacity models.
* Use CloudFront to deliver S3 content securely over HTTPS with cache management.
* Build and validate a highly available Multi-AZ web architecture using ALB, EC2, and RDS.

### Week 4 References

* Lab 000006 - Scaling Applications with EC2 Auto Scaling
* Lab 000010 - Hybrid DNS Management with Amazon Route 53
* Lab 000060 - NoSQL Database Essentials with Amazon DynamoDB
* Lab 000094 - Content Delivery with Amazon CloudFront
* Lab 000101 - Building Highly Available Web Applications
