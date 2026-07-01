---
title: "Week 7 - Final Project Kick-off & Analysis"
date: 2026-04-17
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week Topic

On-site office work, backend API optimization, and mobile sync adjustments.

### Week Objectives

* Work on-site at the AWS Vietnam office on June 1st.
* Collaborate with the team on performance optimizations and mobile UI revisions.
* Minimize API latency by refining database queries and caching strategies.

### Daily Work Log

| Date | Day | Work Items | Lab / Project |
|---|---|---|---|
| 01/06/2026 | Monday | Work on-site at AWS, discussing application optimization strategy and codebase metrics with the mentor. | On-site AWS |
| 02/06/2026 | Tuesday | Refactor JPA/Hibernate database queries in Spring Boot backend, resolving N+1 query issues to minimize MySQL latency. | Backend Code |
| 03/06/2026 | Wednesday | Implement data caching mechanisms for static configuration tables utilizing ElastiCache Redis nodes. | Caching Layer |
| 04/06/2026 | Thursday | Optimize mobile client (React Native) rendering efficiency for heavy transaction lists. | Mobile UI |
| 05/06/2026 | Friday | Debug offline synchronization issues and retry flows when network state changes on mobile. | Integration Testing |

### Expected Outcomes

* Align optimization tasks and obtain technical review from the AWS on-site team.
* Significantly reduce API response times and database CPU load.
* Successfully cache metadata using ElastiCache Redis, reducing RDS read operations.
* Resolve list rendering lag and synchronize data gracefully on the mobile client.

### Week 7 References

* Project Money Manager (Spring Boot API + React Native Mobile Client)
* AWS Services: EC2, RDS MySQL, ElastiCache Redis
