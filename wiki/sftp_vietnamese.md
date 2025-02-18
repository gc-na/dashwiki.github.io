# [Linux] Debian Almquist Shell (dash) sftp Cách sử dụng: Truy cập và quản lý tệp qua giao thức SFTP

## Tổng quan
Lệnh `sftp` (SSH File Transfer Protocol) cho phép người dùng truyền tải và quản lý tệp tin trên máy chủ từ xa một cách an toàn thông qua giao thức SSH. Đây là một công cụ hữu ích cho việc sao chép, tải lên và tải xuống tệp giữa máy tính của bạn và máy chủ.

## Cách sử dụng
Cú pháp cơ bản của lệnh `sftp` như sau:
```
sftp [tùy chọn] [tên người dùng@máy chủ]
```

## Các tùy chọn phổ biến
- `-P <cổng>`: Chỉ định cổng kết nối khác với cổng mặc định (22).
- `-o <tùy chọn>`: Chuyển tiếp các tùy chọn SSH.
- `-v`: Bật chế độ chi tiết để hiển thị thông tin kết nối.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sftp`:

1. Kết nối đến máy chủ SFTP:
   ```bash
   sftp user@hostname
   ```

2. Tải xuống tệp từ máy chủ:
   ```bash
   get filename.txt
   ```

3. Tải lên tệp đến máy chủ:
   ```bash
   put localfile.txt
   ```

4. Liệt kê các tệp trong thư mục hiện tại trên máy chủ:
   ```bash
   ls
   ```

5. Thay đổi thư mục trên máy chủ:
   ```bash
   cd /path/to/directory
   ```

## Mẹo
- Luôn sử dụng kết nối SFTP thay vì FTP để đảm bảo an toàn cho dữ liệu của bạn.
- Kiểm tra quyền truy cập của bạn trên máy chủ để tránh lỗi khi tải lên hoặc tải xuống tệp.
- Sử dụng chế độ chi tiết (`-v`) khi gặp sự cố để có thêm thông tin về lỗi kết nối.