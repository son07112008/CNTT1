Phần 1. Phân tích hệ thốngInput: Dữ liệu cảm biến độ ẩm, nhiệt độ và lệnh thủ công.Output: Tín hiệu bật/tắt máy bơm nước và file log hệ thống.Sơ đồ: Cảm biến gửi dữ liệu về vi điều khiển (SoC) xử lý rồi điều khiển máy bơm thực thi.Phần 2. Nội dung file README.mdMarkdown#  Smart-Farm IoT System

*Hệ thống tự động hóa chăm sóc hoa lan ứng dụng IoT.*

![Sơ đồ hệ thống Smart-Farm](https://static.rangdongstore.vn/product/481206602_982821087278004_1638496667334232020_n.jpg)

## 1. Hướng dẫn cài đặt
```bash
git clone [https://github.com/ptit-it108/smart-farm.git](https://github.com/ptit-it108/smart-farm.git)
cd smart-farm
pip install -r requirements.txt
python main.py
```

2. Tính năng[x] Đọc cảm biến độ ẩm và nhiệt độ 24/7[x] Bật máy bơm tự động khi thiếu nước[ ] Gửi cảnh báo qua Telegram3. Bảng thông sốThiết bịChức năngThông sốCảm biến độ ẩmĐo lượng nước trong đất3.3V - 5VSoCXử lý trung tâmXung nhịp chuẩn4. Chu kỳ CPU (Fetch–Decode–Execute)Fetch: Lấy lệnh từ ô nhớ.Decode: Giải mã thành tín hiệu phần cứng.Execute: Kích hoạt van máy bơm nước.5. Mô hình DIKWData: Nhiệt độ 32°C, độ ẩm 45%.Information: Độ ẩm dưới ngưỡng an toàn.Knowledge: Lan đang có nguy cơ thiếu nước.Wisdom: Tự động bật máy bơm tưới cây.
---

### Phần 3. Xử lý sự cố đầy RAM
```markdown
##  Lưu ý khi đầy RAM
- Dừng tiến trình log: `sudo systemctl stop smart-farm-logger`
- Xóa log cũ: `rm -rf /var/log/smart-farm/*.log`
- Khởi động lại: `sudo systemctl start smar
