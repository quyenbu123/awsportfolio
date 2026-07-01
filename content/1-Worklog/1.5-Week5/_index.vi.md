---
title: "Nhật ký tuần 5 - Tối ưu chi phí Lambda, API Gateway & CloudFormation"
date: 2026-04-17
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Chủ đề tuần

Phát triển mobile app Money Manager, sửa lỗi backend & API, tìm hiểu Lambda và API Gateway.

### Mục tiêu tuần

* Tái cấu trúc và phát triển thêm các tính năng ghi nhận tài chính trên mobile client.
* Fix các lỗi đồng bộ dữ liệu API trên backend.
* Tìm hiểu cơ chế Serverless (Lambda, API Gateway) và Infrastructure as Code (CloudFormation).
* Tham gia sự kiện kết nối công nghệ tại văn phòng AWS.

### Lịch công việc

| Ngày | Thứ | Nội dung công việc | Lab / Dự án |
|---|---|---|---|
| 18/05/2026 | Thứ 2 | Tối ưu hóa UI/UX mobile, cấu hình lưu trữ offline dữ liệu thu nhập/chi tiêu tạm thời. | Mobile Coding |
| 19/05/2026 | Thứ 3 | Tìm hiểu tối ưu chi phí EC2 bằng cách dùng Lambda start/stop instance tự động. Thực hành Lab 000022. | [Lab 000022 - Tối ưu chi phí EC2 với Lambda](https://000022.awsstudygroup.com)|
| 20/05/2026 | Thứ 4 | Nghiên cứu kiến trúc Serverless API với Amazon API Gateway. Thực hành Lab 000055 (Tạo tài nguyên và phương thức). | [Lab 000055 - Tạo và xuất bản API với Amazon API Gateway](https://000055.awsstudygroup.com)|
| 21/05/2026 | Thứ 5 | Đưa API Gateway vào hoạt động thực tế, tích hợp luồng API Gateway với backend. Thực hành Lab 000055 (Deploy API). | [Lab 000055 - Tạo và xuất bản API với Amazon API Gateway](https://000055.awsstudygroup.com)|
| 22/06/2026 | Thứ 6 | Tìm hiểu các khái niệm cơ bản về AWS CloudFormation để quản lý cơ sở hạ tầng tự động bằng code. Thực hành Lab 000037. | [Lab 000037 - AWS CloudFormation](https://000037.awsstudygroup.com)|
| 23/05/2026 | Thứ 7 | Lên văn phòng AWS thực tế, tham gia ngày hội công nghệ cộng đồng AWS Community Day, lắng nghe các bài thuyết trình chuyên sâu. | AWS Community Day |

### Kết quả kỳ vọng

* Sửa đổi giao diện di động ổn định, fix lỗi kết nối CORS ở backend Spring Boot.
* Viết thành công hàm Lambda Python tương tác với API EC2 để tự động tắt/bật máy chủ tiết kiệm điện.
* Thiết lập được REST API trên API Gateway có kích hoạt CORS.
* Viết và deploy thành công template CloudFormation YAML cơ bản.
* Mở rộng mạng lưới quan hệ công nghệ tại sự kiện AWS Community Day.

### Tham chiếu tuần 5

* [Lab 000022 - Tối ưu chi phí EC2 với Lambda](https://000022.awsstudygroup.com)
* [Lab 000055 - Tạo và xuất bản API với Amazon API Gateway](https://000055.awsstudygroup.com)
* [Lab 000037 - AWS CloudFormation](https://000037.awsstudygroup.com)
