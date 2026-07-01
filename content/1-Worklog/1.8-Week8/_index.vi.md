---
title: "Nhật ký tuần 8 - AWS Well-Architected, AWS SAM & Thiết kế kiến trúc"
date: 2026-04-17
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Chủ đề tuần

Họp nhóm thiết kế kiến trúc hạ tầng AWS, sửa lỗi giao diện responsive mobile.

### Mục tiêu tuần

* Vẽ sơ đồ kiến trúc hạ tầng đám mây AWS chi tiết cho Money Manager theo chuẩn AWS Well-Architected.
* Khắc phục các lỗi hiển thị giao diện di động (responsive) trên các tỉ lệ màn hình khác nhau.

### Lịch công việc

| Ngày | Thứ | Nội dung công việc | Lab / Dự án |
|---|---|---|---|
| 08/06/2026 | Thứ 2 | Họp nhóm thiết kế phác thảo kiến trúc VPC (VPC CIDR, chia các Subnet ở nhiều Availability Zone để đảm bảo HA). | Kiến trúc Đám mây |
| 09/06/2026 | Thứ 3 | Cấu hình sơ đồ điều phối traffic: ALB trong Public Subnet hướng traffic vào các EC2 nằm ở Private Subnet. | Network Design |
| 10/06/2026 | Thứ 4 | Thiết kế luồng xử lý bất đồng bộ: SQS queue kết hợp với Worker container để chạy các background jobs (xuất báo cáo). | Async Workflow |
| 11/06/2026 | Thứ 5 | Sửa các lỗi tràn giao diện, lỗi CSS/JSX trên mobile client, kiểm thử hiển thị trên máy Android và iOS. | Mobile Debug |
| 12/06/2026 | Thứ 6 | Rà soát sơ đồ thiết kế hạ tầng theo 5 trụ cột AWS Well-Architected (Bảo mật, Hiệu năng, Tối ưu chi phí, Độ tin cậy, Vận hành xuất sắc). | Well-Architected Review |

### Kết quả kỳ vọng

* Hoàn thành bản thảo sơ đồ kiến trúc mạng VPC multi-AZ có tính dự phòng cao.
* Xác định rõ luồng định tuyến và bảo mật từ bên ngoài qua ALB vào máy chủ nội bộ.
* Tích hợp thành công cấu trúc hàng đợi SQS để xử lý tác vụ gửi mail/báo cáo bất đồng bộ.
* Giao diện mobile hiển thị chuẩn xác, không bị lỗi responsive trên các dòng máy.
* Tài liệu hóa kiến trúc hạ tầng theo đúng chuẩn AWS Well-Architected Framework.

### Tham chiếu tuần 8

* Dự án Money Manager
* AWS Well-Architected Framework
* Sơ đồ hạ tầng: VPC, ALB, EC2 ASG, RDS, SQS, S3, Route 53
