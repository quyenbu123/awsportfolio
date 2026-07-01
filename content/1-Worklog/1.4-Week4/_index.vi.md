---
title: "Nhật ký tuần 4 - Auto Scaling, Route 53, DynamoDB, CloudFront & Kiến trúc HA"
date: 2026-04-17
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Chủ đề tuần

Thiết kế tính năng voice-to-text dự án Money Manager, nghiên cứu Auto Scaling và Route 53.

### Mục tiêu tuần

* Hoàn thiện thiết kế sơ bộ các luồng API chính, nghiên cứu tính năng nhập liệu bằng giọng nói (Voice AI) cho app di động.
* Tìm hiểu cơ chế Amazon EC2 Auto Scaling, Route 53 DNS và thiết kế hệ thống có tính sẵn sàng cao (High Availability).

### Lịch công việc

| Ngày | Thứ | Nội dung công việc | Lab / Dự án |
|---|---|---|---|
| 11/05/2026 | Thứ 2 | Họp nhóm thảo luận thiết kế module audio và luồng chuyển đổi giọng nói thành text cho nhập liệu giao dịch. | Giao diện API |
| 12/05/2026 | Thứ 3 | Tìm hiểu cơ chế mở rộng tự động EC2 Auto Scaling để tự động tăng giảm số lượng instance theo lưu lượng tải. Thực hành Lab 000006. | [Lab 000006 - Tự động co giãn ứng dụng với EC2 Auto Scaling](https://000006.awsstudygroup.com)|
| 13/05/2026 | Thứ 4 | Nghiên cứu giám sát hạ tầng đám mây bằng CloudWatch và quản lý DNS nội bộ bằng Route 53. Thực hành Lab 000008 và Lab 000010. | [Lab 000008 - Tạo giám sát hệ thống với Amazon CloudWatch](https://000008.awsstudygroup.com)|
| 14/05/2026 | Thứ 5 | Cài đặt và sử dụng AWS CLI trên máy chủ EC2 (Linux/Ubuntu) để tự động hóa quản trị đám mây. Thực hành Lab 000011. | [Lab 000011 - Sử dụng AWS CLI trên Amazon EC2](https://000011.awsstudygroup.com)|
| 15/05/2026 | Thứ 6 | Tìm hiểu và triển khai kiến trúc Web đa tầng High Availability (HA) sử dụng ALB và RDS Multi-AZ. Thực hành Lab 000021. | [Lab 000021 - Bài thực hành ứng dụng Web độ sẵn sàng cao](https://000021.awsstudygroup.com)|

### Kết quả kỳ vọng

* Thiết kế sơ đồ luồng dữ liệu xử lý âm thanh cho chức năng Voice AI.
* Cấu hình thành công Auto Scaling Group kết hợp Application Load Balancer (ALB).
* Tạo CloudWatch Alarms và thiết lập các bản ghi DNS với Route 53.
* Viết script chạy AWS CLI tương tác với các tài nguyên AWS.
* Hiểu cách thiết kế hệ thống HA chịu lỗi tốt bằng RDS Multi-AZ và ALB.

### Tham chiếu tuần 4

* [Lab 000006 - Tự động co giãn ứng dụng với EC2 Auto Scaling](https://000006.awsstudygroup.com)
* [Lab 000008 - Tạo giám sát hệ thống với Amazon CloudWatch](https://000008.awsstudygroup.com)
* [Lab 000010 - Quản lý DNS với Amazon Route 53](https://000010.awsstudygroup.com)
* [Lab 000011 - Sử dụng AWS CLI trên Amazon EC2](https://000011.awsstudygroup.com)
* [Lab 000021 - Bài thực hành ứng dụng Web độ sẵn sàng cao](https://000021.awsstudygroup.com)
