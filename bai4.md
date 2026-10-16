I. Thiết kế Kiến trúc Prompt mẫu (File .md)
Markdown
# Thiết lập hệ thống gia sư AI cho sinh viên năm nhất

## Bối cảnh
Tôi là sinh viên năm nhất ngành Công nghệ Thông tin tại PTIT, hiện đang gặp khó khăn khi tìm hiểu về "Mô hình IPO (Input - Process - Output) trong trang trại thông minh". Tôi cần bạn đóng vai một người gia sư kiên nhẫn, giải thích các khái niệm cốt lõi bằng ngôn từ gần gũi, dễ hiểu nhất cho người mới bắt đầu.

## Nội dung và Yêu cầu
- [ ] Giải thích khái niệm Mô hình IPO hoạt động như thế nào trong trang trại thông minh
- [ ] Lấy một ví dụ thực tế cụ thể (ví dụ như hệ thống tưới nước tự động hoặc cảm biến độ ẩm đất)
- [ ] Phân tích rõ 3 thành phần Input, Process, Output tương ứng với ví dụ đó
- [ ] Trình bày ngắn gọn, dễ đọc, không dùng từ ngữ quá hàn lâm

## Không cần
- Không cần giải thích quá sâu về mã nguồn lập trình phần cứng phức tạp hay sơ đồ mạch điện chi tiết
- Không dùng quá nhiều thuật ngữ tiếng Anh chuyên ngành nâng cao nếu chưa được giải thích nghĩa tiếng Việt
II. Xử lý Trường hợp Kiểm thử (Edge Case)
Vấn đề: Nếu AI lỡ tay trả về câu trả lời quá dài dòng hoặc nhồi nhét toàn thuật ngữ tiếng Anh chuyên môn khó hiểu thì phải xử lý thế nào?

Cách khắc phục trong Prompt: ta cần cài thêm ràng buộc phụ ở phần yêu cầu hoặc phần "Không cần" với câu lệnh ép buộc rõ ràng hơn, ví dụ: "Nếu phát hiện thuật ngữ tiếng Anh nào khó, bắt buộc phải dịch nghĩa tiếng Việt ngay bên cạnh và giới hạn câu trả lời trong khoảng 300 từ cho mỗi phần" để kiểm soát độ khó và độ dài chuẩn sinh viên năm nhất.