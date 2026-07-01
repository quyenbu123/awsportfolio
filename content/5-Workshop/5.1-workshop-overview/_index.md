---
title: "Introduction"
date: 2026-07-01
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

### Deploying Infrastructure and Secure Connection to Amazon S3

![Overall network infrastructure and AWS services integration architecture diagram](/images/5-Workshop/5.1-Workshop-overview/architecture-diagram.png?width=70pc&classes=shadow)
*Figure 1. Overall network infrastructure and AWS services integration architecture diagram*

### General Introduction

This report documents the complete hands-on execution of the technical workshop dedicated to building and validating the cloud infrastructure for the **Money Manager** personal finance management platform.

The workshop covers:
* The deployment of a highly secure private network (VPC).
* Separation of frontend API and background Worker instances.
* Integration of data storage tiers: **MySQL RDS**, **Redis ElastiCache**, **DynamoDB**.
* Deployment of **SQS** asynchronous queues.
* Optimization of data transfer costs utilizing **VPC Endpoints** to S3 to shield receipt images (OCR) from public Internet routing and NAT Gateway charges.

Through this practical exercise, we adopted cloud architecture methodologies aligned with the **AWS Well-Architected Framework**, placing specific emphasis on two core pillars: **Security** and **Cost Optimization**.
