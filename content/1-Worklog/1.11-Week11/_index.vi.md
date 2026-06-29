---
title: "Nhật ký tuần 11 - Hoàn thiện Money Manager & Chuẩn bị nộp"
date: 2026-04-17
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Chủ đề tuần

Hoàn thiện sản phẩm Money Manager, tối ưu UI/UX, setup monitoring và chuẩn bị nộp bài

### Mục tiêu tuần

* Polish UI/UX cho cả Web và Mobile, chạy E2E test.
* Setup monitoring, chuẩn bị tài liệu và demo cho việc nộp bài.

### Lịch công việc

| Ngày | Thứ | Nội dung công việc | Lab / Dự án |
|---|---|---|---|
| 29/06/2026 | Thứ 2 | Rà soát và tối ưu UI/UX trên React 19 + Vite (Web) và React Native Expo (Mobile).Kiểm thử cross-platform và responsive cho cả giao diện Web lẫn Mobile.Chạy E2E test các tính năng chính: đăng ký/đăng nhập, quản lý thu chi, chat Nova Money AI. | Project cuối kỳ |
| 30/06/2026 | Thứ 3 | Hoàn thiện tài liệu deploy và hướng dẫn cài đặt hệ thống Money Manager.Cấu hình Amazon CloudWatch: Logs, Metrics, Alarms cho ALB, EC2, RDS, Lambda, SQS.Chuẩn bị rollback script và kiểm tra High Availability trên 2 Availability Zone. | Project cuối kỳ |
| 01/07/2026 | Thứ 4 | Chuẩn bị presentation và kịch bản demo Money Manager.Thực hành demo các tính năng: quản lý thu chi, dự báo tài chính, trợ lý Nova Money, OCR hóa đơn.Hoàn thành README và tài liệu dự án. | Project cuối kỳ |
| 02/07/2026 | Thứ 5 | Kiểm tra tính năng lần cuối, code review tổng thể cho cả backend Spring Boot và frontend React.Viết báo cáo chi tiết: kiến trúc VPC multi-AZ, luồng ALB -> EC2 -> RDS/ElastiCache/DynamoDB.Tạo repository final và cập nhật code. | Project cuối kỳ |
| 03/07/2026 | Thứ 6 | Kiểm tra luồng async: SQS -> EC2 Worker -> Lambda (Report/Invoice) -> S3.Kiểm tra notification flow: Amazon SNS gửi email alert khi ngân sách vượt mức, subscription hết hạn.Backup dữ liệu RDS MySQL, snapshot môi trường và gửi link repository cho giảng viên. | Project cuối kỳ |

### Kết quả kỳ vọng

* UI/UX đã được polish, E2E test pass cho các tính năng chính.
* CloudWatch monitoring hoạt động, rollback script sẵn sàng.
* Tài liệu, slide thuyết trình và demo đã chuẩn bị xong.

### Tham chiếu tuần 11

* Project cuối kỳ — Money Manager (Spring Boot + React 19 + React Native Expo)
* Dịch vụ AWS: CloudWatch, SNS, SQS, Lambda, S3, RDS MySQL backup/snapshot
