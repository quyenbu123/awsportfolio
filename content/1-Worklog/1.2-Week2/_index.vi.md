---
title: "Nhật ký tuần 2 - IAM Roles cho EC2 & Giới thiệu Amazon EC2"
date: 2026-04-17
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

> **Lưu ý:** 30/04 (Ngày Giải phóng) và 01/05 (Ngày Quốc tế Lao động) là ngày nghỉ lễ — tuần này chỉ có 3 ngày làm việc.

### Chủ đề tuần

Đọc hiểu tài liệu kỹ thuật AWS, làm quen AWS Console và quản trị tài nguyên EC2.

### Mục tiêu tuần

* Nghiên cứu cơ chế hoạt động và trường hợp sử dụng thực tế của các dịch vụ đám mây AWS.
* Sử dụng thành thạo AWS Console và quản lý tài nguyên tính toán (EC2).
* Phân tích cách truy cập an toàn từ EC2 đến các dịch vụ lưu trữ khác mà không dùng static key.

### Lịch công việc

| Ngày | Thứ | Nội dung công việc | Lab / Dự án |
|---|---|---|---|
| 27/04/2026 | Thứ 2 | Ôn tập lại cấu hình VPC và phân quyền IAM từ tuần 1. Thiết lập Billing Alarm 5 USD để cảnh báo chi phí phát sinh. | Hệ thống AWS |
| 28/04/2026 | Thứ 3 | Nghiên cứu IAM Roles cho EC2 và mô hình Instance Profile để phân quyền bảo mật không dùng static access key. Thực hành Lab 000048. | [Lab 000048 - IAM Roles cho EC2 (Instance Profile)](https://000048.awsstudygroup.com)|
| 29/04/2026 | Thứ 4 | Tìm hiểu dịch vụ tính toán Amazon EC2. Khởi tạo instance Amazon Linux & Windows, cấu hình key pairs, AMI và security group. Thực hành Lab 000004. | [Lab 000004 - Giới thiệu Amazon EC2](https://000004.awsstudygroup.com)|

### Kết quả kỳ vọng

* Hiểu cách áp dụng Instance Profile để EC2 giao tiếp bảo mật với S3 hay DynamoDB.
* Sử dụng thành thạo các tính năng quản lý tài nguyên trên trang AWS Console.
* Khởi tạo, cấu hình và kết nối thành công vào máy chủ ảo Linux (qua SSH/Session Manager) và Windows (RDP).
* Phân biệt các khái niệm AMI, Instance Types, Security Groups và Key Pairs của EC2.

### Tham chiếu tuần 2

* [Lab 000001 - Tạo tài khoản AWS đầu tiên](https://000001.awsstudygroup.com)
* [Lab 000002 - Quản lý truy cập với AWS IAM](https://000002.awsstudygroup.com)
* [Lab 000003 - Kiến thức mạng cơ bản với Amazon VPC](https://000003.awsstudygroup.com)
* [Lab 000048 - IAM Roles cho EC2 (Instance Profile)](https://000048.awsstudygroup.com)
* [Lab 000004 - Giới thiệu Amazon EC2](https://000004.awsstudygroup.com)
