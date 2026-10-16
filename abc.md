Báo cáo phân tích (I/O)Input (Văn bản thô):Các yêu cầu kỹ thuật về tài liệu hướng dẫn cài đặt cảm biến độ ẩm cho trang trại Lan.Nội dung cần phân biệt rõ giữa văn bản giải thích thông thường và câu lệnh Terminal, mã nguồn Python điều khiển thiết bị, cùng bảng biểu và danh sách kiểm tra công việc.Output (Giao diện render chuyên nghiệp):Tài liệu Markdown hoàn chỉnh sử dụng thành thạo inline code cho lệnh ngắn, code block có màu sắc (syntax highlighting) cho đoạn script Python, bảng so sánh trực quan và task list tương tác.II. Source code (.md)Markdown# Hướng dẫn cài đặt cảm biến độ ẩm cho trang trại Lan

Tài liệu này hướng dẫn các bước thiết lập hệ thống cảm biến và tự động hóa tưới nước cho vườn lan. Khi thao tác trên hệ thống, bạn cần chú ý các ký tự đặc biệt như dấu sao \* hoặc dấu thăng \# phải dùng ký tự escape `\` nếu muốn hiển thị dạng văn bản thông thường.

## 1. Cấu hình môi trường và Terminal

Trước tiên, bạn mở Terminal lên và gõ lệnh cập nhật hệ thống bằng `sudo apt update`, sau đó cài đặt thư viện điều khiển bằng câu lệnh `pip install RPi.GPIO`.

## 2. Đoạn mã Python điều khiển máy bơm

Dưới đây là khối code Python thực hiện đọc giá trị cảm biến và bật tắt máy bơm tự động:

```python
import RPi.GPIO as GPIO
import time

SENSOR_PIN = 17
PUMP_PIN = 27

GPIO.setmode(GPIO.BCM)
GPIO.setup(SENSOR_PIN, GPIO.IN)
GPIO.setup(PUMP_PIN, GPIO.OUT)
3. Bảng so sánh các loại cảm biến độ ẩmTiêu chí so sánhCảm biến đất điện cực cũCảm biến điện dung mới (Capacitive)Độ bềnDễ bị ăn mòn theo thời gianChống gỉ sét tốt hơn, tuổi thọ caoĐộ chính xácThấp, dễ sai số khi khoáng chất đổiCao, đo trực tiếp qua điện dungGiá thànhRẻNhỉnh hơn một chút4. Task List kiểm tra thiết bị trước khi vận hành[x] Kiểm tra kết nối dây nguồn và chân GPIO của cảm biến[x] Chạy thử script Python trên môi trường Terminal[ ] Kiểm tra độ nhạy thực tế của cảm biến trong chậu lan[ ] Cấu hình cơ chế tự động gửi cảnh báo qua Telegram