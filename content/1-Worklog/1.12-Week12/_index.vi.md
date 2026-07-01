---
title: "Nhật ký tuần 12 - Tổng kết dự án cuối kỳ & Nộp bài"
date: 2026-04-17
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Chủ đề tuần

Tổng kết dự án Money Manager — hardening bảo mật, tối ưu chi phí, test recovery và nộp bài

### Mục tiêu tuần

* Hoàn tất các hoạt động tổng kết: bảo mật, chi phí, recovery test.
* Nộp báo cáo, thuyết trình và bàn giao dự án.

### Lịch công việc

| Ngày | Thứ | Nội dung công việc | Lab / Dự án |
|---|---|---|---|
| 06/07/2026 | Thứ 2 | Hỗ trợ xử lý các issue sau deploy và sự cố vận hành.Kiểm tra lại tích hợp dịch vụ bên thứ ba qua NAT Gateway: PayOS, Brevo SMTP, Google Gemini API.Bổ sung license open-source nếu cần. | Project cuối kỳ |
| 07/07/2026 | Thứ 3 | Tổng hợp kiến thức đã học và phác thảo bài blog về triển khai Spring Boot trên AWS.Hardening bảo mật: HTTPS qua Cloudflare, mã hóa dữ liệu, rà soát IAM policies và Security Groups.Ghi lại các vấn đề gặp phải và cách giải quyết trong quá trình triển khai. | Project cuối kỳ |
| 08/07/2026 | Thứ 4 | Review chi phí AWS: RDS MySQL, ElastiCache Redis, EC2 ASG, Lambda, S3, NAT Gateway.Đề xuất phương án tối ưu chi phí (Reserved Instances, Savings Plans).Cập nhật báo cáo cuối và tài liệu kiến trúc. | Project cuối kỳ |
| 09/07/2026 | Thứ 5 | Test recovery và backup restore cho RDS MySQL (multi-AZ failover).Kiểm tra failover ElastiCache Redis trên 2 Availability Zone.Tổng kiểm tra lần cuối, freeze code và chuẩn bị bộ hồ sơ nộp. | Project cuối kỳ |
| 10/07/2026 | Thứ 6 | Nộp báo cáo và thuyết trình dự án Money Manager – Hệ thống Quản lý Tài chính Cá nhân trên AWS.Tổng kết hành trình học AWS và kinh nghiệm triển khai dự án Money Manager.Tự đánh giá bản thân và rút kinh nghiệm. | Project cuối kỳ |

### Kết quả kỳ vọng

* Bảo mật đã hardening, chi phí đã review và có phương án tối ưu.
* Recovery/failover test pass cho RDS MySQL và ElastiCache Redis.
* Nộp bài hoàn tất: báo cáo, slide, demo, repository.

### Tham chiếu tuần 12

* Project cuối kỳ — Money Manager (Spring Boot + React 19 + React Native Expo)
* Trọng tâm: cost review, backup/recovery, security hardening, final presentation
