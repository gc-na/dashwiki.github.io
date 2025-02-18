# [Linux] Debian Almquist Shell (dash) ftp cách sử dụng: Truy cập và quản lý tệp qua giao thức FTP

## Tổng quan
Lệnh `ftp` trong Dash được sử dụng để kết nối và quản lý tệp qua giao thức FTP (File Transfer Protocol). Nó cho phép người dùng tải lên và tải xuống tệp từ máy chủ FTP, cũng như thực hiện các thao tác quản lý tệp cơ bản.

## Cách sử dụng
Cú pháp cơ bản của lệnh `ftp` như sau:
```
ftp [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-i`: Tắt chế độ tương tác, cho phép truyền tệp mà không cần xác nhận.
- `-n`: Ngăn không cho tự động đăng nhập vào máy chủ FTP.
- `-v`: Hiển thị thông tin chi tiết về quá trình truyền tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `ftp`:

1. Kết nối đến máy chủ FTP:
   ```bash
   ftp ftp.example.com
   ```

2. Tải xuống một tệp từ máy chủ:
   ```bash
   get filename.txt
   ```

3. Tải lên một tệp lên máy chủ:
   ```bash
   put localfile.txt
   ```

4. Liệt kê các tệp trong thư mục hiện tại của máy chủ:
   ```bash
   ls
   ```

5. Thoát khỏi phiên FTP:
   ```bash
   bye
   ```

## Mẹo
- Sử dụng tùy chọn `-i` khi bạn cần truyền nhiều tệp mà không muốn xác nhận từng tệp.
- Kiểm tra kết nối mạng của bạn trước khi sử dụng lệnh `ftp` để đảm bảo rằng bạn có thể kết nối đến máy chủ.
- Hãy chắc chắn rằng bạn có quyền truy cập vào máy chủ FTP và các tệp mà bạn muốn quản lý.