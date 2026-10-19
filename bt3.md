xác định thông số vlookup: cột d (tên tác giả) dùng lookup_value là c2, table_array là danhmuctacgia!$a:$e, col_index_num là 2. cột e (phòng) dùng lookup_value là c2, table_array là danhmuctacgia!$a:$e, col_index_num là 4. cột f (thù lao) dùng lookup_value là c2, table_array là danhmuctacgia!$a:$e, col_index_num là 5.

chiến lược xử lý 3 bẫy dữ liệu: dùng trim để cắt khoảng trắng thừa ở mã tác giả, dùng iferror để biến lỗi #N/A thành chữ chưa cập nhật, và dùng dấu $ để cố định vùng tra cứu không bị trôi khi kéo công thức.

các bước thực hiện: chọn ô d2 nhập công thức có lồng trim vlookup iferror rồi kéo xuống ô d81, sau đó sửa col_index_num thành 4 cho cột phòng và 5 cho cột thù lao rồi kéo tiếp cho các cột còn lại.

phần 2 triển khai và chống lỗi

công thức hoàn chỉnh cho ô d2: =iferror(vlookup(trim(c2), danhmucctacgia!$a:$e, 2, false), "chưa cập nhật")

công thức ô e2 là =iferror(vlookup(trim(c2), danhmucctacgia!$a:$e, 4, false), "chưa cập nhật") và ô f2 là =iferror(vlookup(trim(c2), danhmucctacgia!$a:$e, 5, false), "chưa cập nhật"). chỉ cần đổi số cột vì cấu trúc bảng tra cứu giống nhau, không phải viết lại từ đầu.

nếu bỏ dấu $ thì khi kéo công thức từ d2 xuống d5, vùng tra cứu sẽ bị trôi theo số dòng thành danhmuctacgia!a4:e8, làm lệch bảng và trả kết quả sai.