# [Hệ điều hành] Debian Almquist Shell (dash) scp: [sao chép tệp qua SSH]

## Tổng quan
Lệnh `scp` (Secure Copy Protocol) được sử dụng để sao chép tệp giữa các máy tính qua giao thức SSH. Nó cho phép người dùng truyền tải tệp một cách an toàn giữa các hệ thống khác nhau.

## Cách sử dụng
Cú pháp cơ bản của lệnh `scp` như sau:
```bash
scp [options] [source] [destination]
```

## Các tùy chọn phổ biến
- `-r`: Sao chép thư mục và tất cả các tệp bên trong.
- `-P`: Chỉ định cổng SSH khác với cổng mặc định (22).
- `-i`: Sử dụng tệp khóa riêng để xác thực.
- `-v`: Hiển thị thông tin chi tiết về quá trình sao chép (verbose).

## Ví dụ phổ biến
- Sao chép tệp từ máy cục bộ đến máy từ xa:
```bash
scp file.txt user@remote_host:/path/to/destination
```

- Sao chép tệp từ máy từ xa về máy cục bộ:
```bash
scp user@remote_host:/path/to/file.txt /local/destination
```

- Sao chép một thư mục từ máy cục bộ đến máy từ xa:
```bash
scp -r /local/directory user@remote_host:/path/to/destination
```

- Sao chép tệp qua cổng SSH tùy chỉnh:
```bash
scp -P 2222 file.txt user@remote_host:/path/to/destination
```

## Mẹo
- Luôn kiểm tra quyền truy cập tệp và thư mục trước khi sao chép để tránh lỗi.
- Sử dụng tùy chọn `-v` để gỡ lỗi nếu gặp vấn đề trong quá trình sao chép.
- Đảm bảo rằng SSH được cài đặt và cấu hình đúng trên cả hai máy tính để sử dụng `scp` hiệu quả.