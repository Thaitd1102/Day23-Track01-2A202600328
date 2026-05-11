# 03 - Product ROI Dashboard v2

## Part A: Adoption Context

* **Sản phẩm:** Hệ thống Tư vấn Tuyển sinh Thông minh (AI Chatbot tích hợp RAG).
* **Người dùng chính:** Học sinh/Phụ huynh (truy vấn) và Cán bộ tuyển sinh (giám sát).
* **Pain Points:** Cán bộ quá tải vì trả lời câu hỏi lặp lại; lo sợ AI "ảo giác" (hallucination) gây sai lệch thông tin chính thống; rủi ro bị tấn công prompt injection.
* **2 Workflow chính:**
    1.  **Hỏi đáp tự động có dẫn chứng:** AI nhận diện ý định -> Truy xuất Ground Truth từ database -> Trả lời kèm URL dẫn chứng từ website nhà trường.
    2.  **Xử lý ca khó (Escalation):** AI phát hiện không có dữ liệu hoặc câu hỏi nhạy cảm -> Chuyển luồng cho Cán bộ tư vấn kèm tóm tắt bối cảnh.
* **Con người kiểm tra ở đâu:** Duyệt các câu trả lời cho ca phức tạp (điểm chuẩn, học bổng); Audit ngẫu nhiên 5% log chat hằng tuần để kiểm tra độ khớp của trích dẫn.
* **Xử lý khi AI sai:** Ngắt kết nối chat, tự động gửi lời xin lỗi và thông báo "Cố vấn sẽ liên hệ lại sau 5 phút"; ghi log lỗi vào hệ thống giám sát.
* **Rào cản ADKAR:** **Trust (Niềm tin)** - Cán bộ lo ngại AI tự bịa số liệu.
* **3 Tactics tăng Adoption:**
    1.  **Force-citation:** Ép AI luôn hiển thị nguồn link chính thức.
    2.  **Human-in-the-loop checklist:** Quy trình kiểm duyệt nhanh cho agent.
    3.  **QA Dashboard hằng tuần:** Công khai tỷ lệ AI trả lời đúng nguồn.

---

## Part B: ROI Dashboard (Đã sửa sau Red-team)

| Layer | Metric | Baseline | Target | Data Source | Owner | Red-team Risk | Fix (v2) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Product / Activation** | % Chat có Citation (trích dẫn) hợp lệ | 0% | > 85% | Chat Log | Tech Lead | Link trích dẫn có thể dẫn tới văn bản cũ | Thêm tool auto-check version tài liệu mỗi 24h |
| **Workflow / Quality** | Tỷ lệ Override (Cán bộ phải sửa) | 100% | < 10% | Admin Dashboard | Head of Admissions | Cán bộ lười check, cứ thế nhấn Approve | Random audit chéo giữa các cán bộ |
| **Workflow / Trust** | Citation Accuracy (Độ chính xác nguồn) | N/A | > 98% | QA Sample | CX Lead | AI trích dẫn link thật nhưng nội dung không khớp | Ép AI trích xuất đoạn văn (snippet) trước khi trả lời |
| **Value** | Cost per Resolved Ticket (Chi phí/ca) | 25k VNĐ | < 5k VNĐ | Finance Log | Project Manager | Cắt giảm nhân sự quá nhanh gây giảm CSAT | Duy trì đội trực ca khó để giữ chất lượng |

---

## Part C: Dashboard Mock (Mô phỏng)

- **[Product Coverage]:** 70% hội thoại được AI xử lý kèm dẫn chứng.
- **[Quality Goal]:** Override Rate hiện tại 7% (Màu Xanh 🟢).
- **[Trust Indicator]:** Citation Accuracy 99% (Màu Xanh 🟢).
- **[Value]:** Tiết kiệm ~20 triệu VNĐ tiền nhân công/tháng.

---

## Part D: Decision Memo

1.  **Đề xuất:** **Continue** (Tiếp tục triển khai rộng rãi cho mùa tuyển sinh 2026).
2.  **Metric mạnh nhất:** **Citation Accuracy**. Đây là dẫn chứng thép để chứng minh AI không "bịa lời", giúp cán bộ an tâm nhả việc.
3.  **Thay đổi sau Red-team:** Đã bổ sung cột "Fix" cho rủi ro link tài liệu bị cũ (Stale links) và thêm cơ chế audit chéo để tránh việc Cán bộ duyệt ẩu.
4.  **Hành động trước khi Scale:** Hoàn thiện bộ Eval (kiểm thử) cho 100 câu hỏi "bẫy" thường gặp của sinh viên.