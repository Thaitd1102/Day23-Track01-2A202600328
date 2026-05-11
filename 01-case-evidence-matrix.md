# 01 - Case Evidence Matrix (Bài tập cá nhân)

**Case được phân tích:** Morgan Stanley (Thành công / Tín hiệu tốt)

**1. AI được dùng trong workflow nào?**
AI (Morgan Stanley Assistant) được tích hợp vào quy trình truy xuất kiến thức nội bộ của các Cố vấn tài chính. Thay vì tìm kiếm thủ công qua hàng ngàn trang tài liệu, cố vấn dùng AI để truy vấn thông tin, tóm tắt báo cáo và chuẩn bị nội dung tư vấn cho khách hàng.

**2. Họ đo metric gì?**
- Tỷ lệ áp dụng (Adoption rate): 98% đội ngũ cố vấn sử dụng tool.
- Đánh giá chất lượng (Eval framework): Đo lường thông qua phản hồi từ chuyên gia và các chốt chặn tuân thủ (compliance controls) khắt khe của ngành tài chính.

**3. Metric đó chứng minh được gì?**
Chứng minh được rằng: Người dùng sẽ sẵn sàng đưa AI vào luồng công việc thực tế (workflow) nếu hệ thống có **kiến trúc niềm tin (trust architecture)** vững chắc. Cố vấn dám dùng AI vì nó bị ràng buộc bởi các quy định kiểm duyệt rủi ro, đảm bảo thông tin đưa ra là có cơ sở.

**4. Metric đó chưa chứng minh được gì?**
Chưa chứng minh được chính xác mức độ hiệu quả kinh doanh cuối cùng (Business Value). Cụ thể, không rõ hệ thống đã giúp tiết kiệm bao nhiêu giờ làm việc thực tế cho mỗi phiên tư vấn, hay có làm tăng tỷ lệ chốt sale/tăng trưởng doanh thu từ khách hàng hay không.

**5. Còn thiếu metric nào?**
- Thời gian tiết kiệm được trên mỗi tác vụ (Task-time reduction).
- Tỷ lệ giảm sai sót/làm lại (Rework reduction).
- Mức độ hài lòng của khách hàng cuối (CSAT) sau khi nhận được tư vấn có sự hỗ trợ của AI.

**6. Bài học nào áp dụng được vào dashboard của nhóm?**
**Bài học cốt lõi:** Khi áp dụng AI vào các lĩnh vực có rủi ro cao (High-stakes) như tư vấn tài chính hay **tư vấn tuyển sinh**, tuyệt đối không thể chỉ đo "Số lượt dùng" (Usage). 
- Dashboard bắt buộc phải có các chỉ số đo lường **Niềm tin (Trust)** và **Chất lượng (Quality)**. 
- Nếu không xây dựng được cơ chế kiểm duyệt (ép AI phải có **trích dẫn/dẫn chứng xác thực** từ Ground Truth), người dùng (Cán bộ tư vấn) sẽ nơm nớp lo sợ AI "ảo giác" và không bao giờ dám áp dụng nó vào vận hành thực tế.