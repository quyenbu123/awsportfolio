---
title: "Bài thực hành"
date: 2026-06-29
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

Bài thực hành thiết lập hệ thống và kết nối bảo mật đến S3 cho dự án Money Manager:

### [5.1. Giới thiệu](5.1-workshop-overview/)
Giới thiệu tổng quan về workshop xây dựng và kiểm thử hệ thống hạ tầng đám mây cho dự án quản lý tài chính cá nhân Money Manager theo tiêu chuẩn AWS Well-Architected.

### [5.2. Các bước chuẩn bị](5.2-prerequiste/)
Các bước thiết lập tài khoản AWS, tạo khóa kết nối CLI thông qua IAM Access Keys, cài đặt môi trường máy trạm local (Node.js, JDK, Maven, Docker) và xác định vùng hạ tầng Singapore.

### [5.3. Các bước thực hiện chi tiết](5.3-implementation-steps/)
Chi tiết 4 bước triển khai thực tế: thiết lập mạng riêng VPC & EC2; cấu hình cơ sở dữ liệu RDS MySQL & ElastiCache Redis OSS; tích hợp lưu trữ DynamoDB & hàng đợi AWS SQS; cấu hình bảo mật Amazon S3 & VPC Endpoints.

### [5.4. Kiểm tra kết quả & thực nghiệm](5.4-validation/)
Thử nghiệm kiểm thử định tuyến DNS nội bộ, phân quyền bảo mật S3 bucket, lưu trữ DynamoDB & truyền tải tin nhắn SQS, cùng kết quả đo lường cải thiện độ trễ và tối ưu chi phí NAT Gateway.

### [5.5. Dọn dẹp tài nguyên](5.5-cleanup/)
Quy trình dọn dẹp các tài nguyên hạ tầng thử nghiệm (S3 objects, VPC Endpoints, DNS Records, Docker cache) sau khi hoàn thành thực hành để tránh phát sinh chi phí phát sinh.