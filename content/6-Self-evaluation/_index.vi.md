---
title: "Tự đánh giá"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Sau khi kết thúc giai đoạn học tập nền tảng và bước vào triển khai thực tế cho dự án, em muốn dành thời gian rà soát lại chặng đường thực tập vừa qua. Đây là cơ hội tốt để em nhìn nhận khách quan về những kỹ năng đã đạt được và những điểm còn hạn chế cần tiếp tục hoàn thiện.

Thời gian đầu tiếp cận các dịch vụ đám mây thực tế, em gặp không ít khó khăn trong việc kết hợp các cấu hình mạng và bảo mật. Tuy nhiên, qua quá trình tự nghiên cứu tài liệu kết hợp thực hành lab hàng tuần, em đã từng bước làm chủ được quy trình thao tác và hình thành tư duy hệ thống tốt hơn. Dù vậy, em hiểu rằng đây mới chỉ là những nền tảng ban đầu và bản thân cần nỗ lực nhiều hơn nữa.

### Bảng tự đánh giá

| Tiêu chí | Đánh giá | Nhận xét |
|---|---|---|
| Kiến thức | Khá | Hiểu và tích hợp tốt các dịch vụ AWS cốt lõi (IAM, VPC, S3, RDS, DynamoDB, SQS, API Gateway,...); cần trau dồi thêm về viết code hạ tầng IaC và cấu hình hybrid networking. |
| Khả năng học hỏi | Tốt | Tự nghiên cứu tài liệu chính thống của AWS nhanh, chủ động giải quyết các yêu cầu tích hợp SDK v2 mới vào dự án. |
| Tính chủ động | Khá | Tích cực đề xuất giải pháp nhập liệu giọng nói (Voice Input) cho ứng dụng di động; đôi khi cần quản lý thứ tự ưu tiên tốt hơn khi công việc dồn dập. |
| Kỷ luật | Tốt | Hoàn thành đúng hạn lộ trình đề ra, thực hiện nghiêm túc việc dọn dẹp tài nguyên test để tối ưu hóa chi phí sử dụng cloud. |
| Giao tiếp | Khá | Trình bày tài liệu kỹ thuật và API rõ ràng; cần rèn luyện thêm cách diễn đạt ngắn gọn, trực diện vào vấn đề. |
| Teamwork | Khá | Phối hợp tốt với nhóm để tích hợp API backend với giao diện mobile; tích cực tham gia thảo luận nhóm và các sự kiện công nghệ. |
| Giải quyết vấn đề | Khá | Đã hình thành tư duy debug hệ thống thông qua tra cứu log CloudWatch, kiểm tra Security Group và Route Table thay vì lúng túng làm lại từ đầu. |
| Đóng góp cho dự án | Khá | Đảm nhận chính phần xây dựng giao diện di động, viết các bài đăng chia sẻ kiến thức (Blog) và tham gia đầy đủ các hoạt động của chương trình. |

### Những gì em thấy em tiến bộ

Sau một thời gian trải nghiệm, em cảm thấy mình đã có những bước tiến rõ rệt cả về tư duy lẫn kỹ năng thực tế:

* **Làm chủ quy trình cấu hình AWS:** Từ chỗ chỉ nắm lý thuyết suông, em đã tự tay thiết lập được phân hệ mạng VPC bảo mật, cấu hình API Gateway kết nối với Lambda, tạo cơ sở dữ liệu DynamoDB và triển khai VPC Endpoints để tối ưu chi phí khi kết nối đến S3.
* **Hình thành tư duy gỡ lỗi (Troubleshooting):** Mỗi khi hệ thống gặp sự cố kết nối hay phân quyền, em không còn hoang mang mà đã biết cách chủ động kiểm tra các lớp bảo mật như Security Group, Route Table, IAM Policy, cũng như đọc log trên CloudWatch để tìm ra đúng nguyên nhân gốc rễ.
* **Rèn luyện phương pháp tự nghiên cứu:** Nhờ duy trì lộ trình học nghiêm túc, em đã hình thành thói quen chủ động đọc tài liệu kỹ thuật, nghiên cứu các Whitepapers của hãng và luôn thử nghiệm kỹ lưỡng ở quy mô nhỏ trước khi áp dụng thực tế.
* **Ý thức kiểm soát tài nguyên đám mây:** Em hiểu rất rõ việc cấu hình sai hoặc quên tắt dịch vụ trên cloud sẽ ảnh hưởng thế nào đến chi phí. Vì vậy, em luôn có ý thức rà soát, dọn dẹp các tài nguyên thử nghiệm để tránh lãng phí ngân sách.
* **Nâng cao kỹ năng viết và diễn đạt:** Việc duy trì viết worklog hàng ngày và chia sẻ các bài blog kỹ thuật hàng tuần đã giúp em cải thiện đáng kể khả năng diễn đạt, biết cách sắp xếp và truyền tải các thông tin công nghệ phức tạp một cách mạch lạc, dễ hiểu hơn.

### Những gì em cần cải thiện

Bên cạnh những kết quả đã đạt được, em tự nhận thấy bản thân vẫn còn những điểm khuyết và cần tập trung cải thiện trong thời gian tới:

* **Kỹ năng thiết kế kiến trúc tổng thể:** Em vẫn còn chút lúng túng khi đứng trước một bài toán lớn đòi hỏi phải tự đề xuất giải pháp kiến trúc hạ tầng từ con số 0 mà không có tài liệu hay hướng dẫn cụ thể từ trước.
* **Mức độ thành thạo IaC (Infrastructure as Code):** Dù đã biết viết template CloudFormation cơ bản, em thấy mình vẫn còn phụ thuộc khá nhiều vào việc click tay trên giao diện AWS Console. Mục tiêu sắp tới của em là chuyển dịch hoàn toàn sang quản trị hạ tầng bằng code.
* **Kiến thức mạng nâng cao:** Các khái niệm mạng phức tạp hơn như Transit Gateway hay Route 53 Resolver trong mô hình Hybrid Cloud vẫn là một thách thức lớn, đòi hỏi em phải dành nhiều thời gian để nghiên cứu sâu và kỹ hơn.
* **Kinh nghiệm tích hợp CI/CD tự động:** Em chưa có nhiều cơ hội thực hành thực tế trong việc thiết lập một pipeline tự động hóa hoàn chỉnh để deploy sản phẩm một cách bài bản từ môi trường staging lên production.
* **Kỹ năng quản lý thời gian:** Em cần học cách phân bổ thời gian khoa học và kỷ luật hơn để có thể cân bằng tốt giữa việc hoàn thành các bài tập trên trường với tiến độ thực hiện các bài tập thực hành thực tập.

### Nhìn chung

Trải qua giai đoạn học tập vừa qua, em tự nhận thấy bản thân đã có sự chuyển biến rõ rệt từ việc "nắm bắt khái niệm" sang "thực hành tự lập và tự giải quyết vấn đề". Đây là nền móng quan trọng để em tiếp tục lấp đầy các khoảng trống kỹ thuật trong giai đoạn triển khai dự án thực tế tiếp theo.