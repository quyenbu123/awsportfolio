---
title: "Resource Cleanup"
date: 2026-07-01
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

After completing the technical workshop session, clean up the testing infrastructure resources to avoid recurring charges on the AWS account:

1. **S3 Storage:** Delete all temporary testing objects uploaded to S3 bucket `botdevgroup-documents` to eliminate monthly storage fees.
2. **Interface VPC Endpoint:** Delete the Interface VPC Endpoint `vpce-s3-interface` to release the ENIs and halt the hourly instance charges associated with AWS PrivateLink.
3. **Gateway VPC Endpoint:** Detach the S3 Gateway VPC Endpoint from the Private Subnet Route Tables to revert the routing configuration of the VPC.
4. **DNS & Security Groups:** Remove testing Inbound/Outbound DNS Resolver Rules and associated Security Group rules from the configurations.
5. **EC2 Clean:** Execute the Docker system prune command (`docker system prune -af`) on the EC2 instance to reclaim unused EBS disk storage space.
