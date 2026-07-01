---
title: "Nhật ký tuần 10 - Bảo mật, CI/CD & Kiểm thử cho dự án cuối kỳ"
date: 2026-04-17
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Chủ đề tuần

Lập kế hoạch deploy production, deploy dự án lên domain botdevgroup.me và viết báo cáo.

### Mục tiêu tuần

* Thống nhất phương án và lên kế hoạch đưa ứng dụng di động và API lên môi trường production.
* Deploy thực tế hệ thống hạ tầng và ứng dụng lên AWS thông qua tên miền chính thức \`botdevgroup.me\`.
* Bắt đầu soạn thảo các chương cốt lõi trong báo cáo thực tập tốt nghiệp.

### Lịch công việc

| Ngày | Thứ | Nội dung công việc | Lab / Dự án |
|---|---|---|---|
| 22/06/2026 | Thứ 2 | Họp nhóm rà soát cấu hình production: biến môi trường bảo mật, credentials, IP whitelist và các thiết lập API. | Kế hoạch Deploy |
| 23/06/2026 | Thứ 3 | Cấu hình Route 53 DNS và tích hợp dịch vụ Cloudflare WAF bảo vệ cổng ALB, trỏ tên miền chính botdevgroup.me về AWS. | Domain & DNS |
| 24/06/2026 | Thứ 4 | Deploy các container API và Worker lên các máy chủ EC2 thực tế trong Private Subnet, kết nối RDS MySQL và ElastiCache. | Deployment |
| 25/06/2026 | Thứ 5 | Bắt đầu viết nội dung báo cáo thực tập: chương Giới thiệu tổng quan về đơn vị thực tập, phân tích yêu cầu phần mềm. | Viết Báo cáo |
| 26/06/2026 | Thứ 6 | Soạn thảo chương mô tả Kiến trúc hạ tầng AWS, mô tả chi tiết cách thiết lập bảo mật và tối ưu chi phí trong báo cáo. | Viết Báo cáo |

### Kết quả kỳ vọng

* Chốt bảng kiểm tra (checklist) triển khai sản phẩm thực tế.
* Tên miền botdevgroup.me trỏ thành công về hệ thống AWS và được bảo vệ bởi Cloudflare proxy.
* Ứng dụng chạy trực tuyến ổn định trên môi trường production, API phản hồi tốt.
* Hoàn thành bản thảo 2 chương đầu tiên của Báo cáo thực tập tốt nghiệp.

### Tham chiếu tuần 10

* Dự án Money Manager
* Domain: botdevgroup.me (Cloudflare DNS & WAF)
* Tài liệu báo cáo thực tập tốt nghiệp
