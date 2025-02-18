# [Hệ điều hành] Debian Almquist Shell (dash) mtr Cách sử dụng: Kiểm tra kết nối mạng

## Overview
Lệnh `mtr` (My Traceroute) kết hợp giữa chức năng của `traceroute` và `ping`, giúp người dùng kiểm tra và phân tích đường đi của gói tin trong mạng. Nó cung cấp thông tin chi tiết về các nút mạng mà gói tin đi qua và thời gian phản hồi từ mỗi nút.

## Usage
Cú pháp cơ bản của lệnh `mtr` như sau:
```bash
mtr [options] [arguments]
```

## Common Options
- `-r`: Chạy trong chế độ báo cáo, hiển thị kết quả một lần và thoát.
- `-c <count>`: Xác định số lượng gói tin sẽ được gửi đến mỗi nút.
- `-i <interval>`: Đặt khoảng thời gian giữa các gói tin (tính bằng giây).
- `-p`: Chạy trong chế độ chỉ định cổng, cho phép kiểm tra một cổng cụ thể.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mtr`:

1. Kiểm tra kết nối đến một địa chỉ IP hoặc tên miền:
   ```bash
   mtr google.com
   ```

2. Chạy lệnh `mtr` với chế độ báo cáo và chỉ định số lượng gói tin:
   ```bash
   mtr -r -c 10 google.com
   ```

3. Kiểm tra kết nối đến một địa chỉ IP với khoảng thời gian giữa các gói tin là 2 giây:
   ```bash
   mtr -i 2 8.8.8.8
   ```

4. Kiểm tra một cổng cụ thể trên một địa chỉ IP:
   ```bash
   mtr -p 80 example.com
   ```

## Tips
- Sử dụng `mtr` với quyền root để có được thông tin chi tiết hơn về các nút mạng.
- Thực hiện `mtr` với tùy chọn `-r` để nhận báo cáo nhanh chóng mà không cần phải xem liên tục.
- Nếu bạn gặp vấn đề về kết nối, hãy thử chạy `mtr` với các địa chỉ khác nhau để xác định vị trí của sự cố.