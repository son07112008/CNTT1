Bài 6 : Hoàn thiện bộ hồ sơ triển khai nền tảng Smart-Home
Phần 1. Phân tích: Excel "Xấu" vs "Đúng"
Bảng Excel "Xấu": Dùng Merge Cell trong vùng dữ liệu, thiếu Header chuẩn, chèn dòng tổng cộng ở giữa bảng, gây lỗi bộ lọc (AutoFilter) và hàm (VLOOKUP).
Bảng Excel "Đúng": Cấu trúc phẳng, đúng một dòng tiêu đề duy nhất, mỗi cột một kiểu dữ liệu đồng nhất, tối ưu cho trích xuất và Pivot Table.
Phần 2. Triển khai: Học liệu Smart-Home
1. Cấu trúc Heading (1, 2, 3) cho file Word
1. Giới thiệu tổng quan hệ thống Smart-Home
2. Mô tả nghiệp vụ nền tảng IoT Smart-Home
3. Yêu cầu chức năng và phi chức năng
2. Tra cứu hoa hồng bằng Excel (VLOOKUP)
Cú pháp: =VLOOKUP(vt1, vt2, vt3, o)
Ứng dụng: Tự động trích xuất tỷ lệ hoa hồng môi giới dựa theo mã gói thiết bị.
3. Thiết kế Slide Pitch Deck (Rule 10/20/30)
Quy mô: Tối đa 10 slide thuyết trình trong vòng 20 phút.
Nguyên tắc: 1 Slide - 1 Thông điệp cốt lõi, kết hợp không gian trắng (White Space) để làm nổi bật số liệu và biểu đồ.
Phần 3. Kiểm thử: Khắc phục lỗi trôi vùng dữ liệu (VLOOKUP)
Nguyên nhân: Kéo công thức mà không cố định vùng tra cứu khiến địa chỉ bảng tự dịch chuyển, trả về lỗi #N/A.
Cách khắc phục: dùng f4 để thêm dấu tuyệt đối $ vào tọa độ bảng