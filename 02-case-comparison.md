# 02 - Case Comparison & Lesson Learned

## Bảng So Sánh Cặp Case: Morgan Stanley (Thành công) vs Klarna (Cảnh báo)

| Tiêu chí | Case Thành công: Morgan Stanley | Case Cảnh báo: Klarna |
| :--- | :--- | :--- |
| **Workflow (Quy trình)** | Cố vấn tài chính dùng AI truy xuất kiến thức nội bộ để tư vấn cho khách. | AI Chatbot trực tiếp tiếp nhận và xử lý yêu cầu của khách hàng thay agent. |
| **Metric (Chỉ số)** | Tỷ lệ sử dụng (98% cố vấn dùng) + Đánh giá chất lượng từ chuyên gia. | Số lượng hội thoại xử lý (2.3 triệu), Containment rate (Tự giải quyết $2/3$ số chat). |
| **Prove (Chứng minh được)** | Người dùng thực sự đưa AI vào workflow khi hệ thống có chốt chặn rủi ro đáng tin cậy. | AI có khả năng mở rộng (scale) để gánh vác khối lượng lớn các tác vụ lặp lại. |
| **Not Prove (Chưa CM được)** | Thời gian thực tế tiết kiệm được cho mỗi phiên làm việc/doanh thu tăng thêm. | Tỷ lệ tự giải quyết cao không chứng minh được chất lượng dịch vụ hoặc độ hài lòng của khách. |
| **Missing Metric (Chỉ số thiếu)** | Thời gian hoàn thành tác vụ (Task-time reduction), Tỷ lệ làm lại (Rework). | Độ hài lòng (CSAT) theo độ phức tạp, Tỷ lệ khiếu nại lại, Tỷ lệ bàn giao cho người (Handoff) thành công. |

## Bài học cho Dashboard của hệ thống Tuyển sinh:
Tuyệt đối không đo ROI bằng "Số lượng tin nhắn AI trả lời được" (Bẫy Klarna). Trong lĩnh vực giáo dục/tuyển sinh, một câu trả lời sai (ảo giác/hallucination) có thể gây khủng hoảng truyền thông. 

Do đó, Dashboard phải tập trung vào **Trust & Quality Metrics** (giống Morgan Stanley): Buộc AI phải đính kèm **link trích dẫn (Dẫn chứng)** từ tài liệu chính thống trong mọi câu trả lời. Chỉ số quan trọng nhất sẽ là "Tỷ lệ trích dẫn chính xác" (Citation Accuracy) và "Tỷ lệ ghi đè của con người" (Override rate).