# [Hệ điều hành] Debian Almquist Shell (dash) telnet: Kết nối tới máy chủ từ xa

## Tổng quan
Lệnh `telnet` được sử dụng để kết nối tới máy chủ từ xa qua giao thức Telnet. Nó cho phép người dùng truy cập và quản lý các hệ thống từ xa thông qua dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `telnet` như sau:
```
telnet [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-l <tên người dùng>`: Đặt tên người dùng để đăng nhập vào máy chủ.
- `-d`: Bật chế độ gỡ lỗi.
- `-n <tên tệp>`: Ghi lại thông tin phiên làm việc vào tệp chỉ định.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `telnet`:

1. Kết nối tới một máy chủ:
   ```sh
   telnet example.com 23
   ```

2. Kết nối tới một máy chủ với tên người dùng cụ thể:
   ```sh
   telnet -l user example.com 23
   ```

3. Kết nối tới một máy chủ và ghi lại phiên làm việc:
   ```sh
   telnet -n session.log example.com 23
   ```

## Mẹo
- Hãy chắc chắn rằng máy chủ bạn đang cố gắng kết nối hỗ trợ giao thức Telnet.
- Sử dụng Telnet chỉ trong các mạng an toàn, vì dữ liệu không được mã hóa.
- Nếu có thể, hãy xem xét sử dụng SSH thay thế cho Telnet để bảo mật tốt hơn.