# 04 - Reflection

Trong quá trình xây dựng Dashboard cho hệ thống Tư vấn Tuyển sinh, chỉ số mà tôi trăn trở và quyết định sửa đổi mạnh mẽ nhất sau phiên Red-team chính là **Citation Accuracy (Độ chính xác của trích dẫn)**. 

Ban đầu, tôi chỉ tập trung vào "Số lượng tin nhắn AI trả lời được", nhưng qua các case study như Klarna hay Morgan Stanley, tôi nhận ra rằng trong giáo dục, việc nói nhanh không quan trọng bằng nói đúng. Một liên kết dẫn chứng (URL) sai lệch không chỉ làm mất niềm tin của học sinh mà còn có thể gây hậu quả pháp lý cho nhà trường. 

Giả định ban đầu của tôi là chỉ cần có link là người dùng sẽ tin. Tuy nhiên, sau phản biện, tôi hiểu rằng link phải dẫn đến đúng "Ground Truth" và phải được cập nhật phiên bản mới nhất. Vì vậy, tôi đã bổ sung cơ chế kiểm soát phiên bản tài liệu (Document Versioning) vào workflow. Bài học lớn nhất tôi rút ra là: AI chỉ thực sự được "adopt" (áp dụng) khi chúng ta giải quyết được bài toán trách nhiệm thông qua các dẫn chứng không thể chối cãi.