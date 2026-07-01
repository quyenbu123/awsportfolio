---
title: "Week 8 - AWS Well-Architected, AWS SAM & Architecture Design"
date: 2026-04-17
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week Topic

AWS infrastructure design meeting and mobile responsive fixes.

### Week Objectives

* Draft the detailed AWS cloud architecture diagram for Money Manager aligned with AWS Well-Architected best practices.
* Resolve mobile client responsive layout issues across various screen aspect ratios.

### Daily Work Log

| Date | Day | Work Items | Lab / Project |
|---|---|---|---|
| 08/06/2026 | Monday | Team session mapping out the custom VPC configuration (multi-AZ subnets, CIDR boundaries for high availability). | Cloud Architecture |
| 09/06/2026 | Tuesday | Design public/private subnet routing, placing the ALB in public subnets and backend EC2 instances in private subnets. | Networking |
| 10/06/2026 | Wednesday | Design asynchronous background pipelines using SQS queues and Worker containers for heavy file generation. | Asynchronous Jobs |
| 11/06/2026 | Thursday | Fix CSS/JSX overflow errors on the mobile UI, verifying responsive layouts on both Android and iOS devices. | UI Refactoring |
| 12/06/2026 | Friday | Evaluate the drafted architecture against the five pillars of the AWS Well-Architected Framework. | Well-Architected |

### Expected Outcomes

* Completed VPC network diagram detailing subnets, route tables, and gateways across two AZs.
* Clear security policy defining access routes through the Application Load Balancer.
* Defined SQS queue specifications and message schemas for email/report jobs.
* Pixel-perfect mobile UI layouts running correctly on multiple phone sizes.
* Technical architecture notes aligned with AWS Well-Architected pillars.

### Week 8 References

* Project Money Manager
* AWS Well-Architected Framework
* Cloud Architecture tools (Draw.io)
