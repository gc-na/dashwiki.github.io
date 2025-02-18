# [Hệ điều hành] Debian Almquist Shell (dash) strace cách sử dụng: Theo dõi hệ thống cuộc gọi

## Tổng quan
Lệnh `strace` được sử dụng để theo dõi các cuộc gọi hệ thống và tín hiệu mà một chương trình thực hiện. Điều này rất hữu ích cho việc gỡ lỗi và phân tích hành vi của các ứng dụng, giúp người dùng hiểu rõ hơn về cách mà các chương trình tương tác với hệ điều hành.

## Cách sử dụng
Cú pháp cơ bản của lệnh `strace` như sau:

```bash
strace [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-e trace=<loại>`: Chỉ theo dõi các cuộc gọi hệ thống cụ thể, ví dụ như `file`, `process`, hoặc `network`.
- `-o <tên_tập_tin>`: Ghi đầu ra của `strace` vào một tập tin thay vì hiển thị trên màn hình.
- `-p <pid>`: Theo dõi một tiến trình đang chạy với ID tiến trình (PID) đã cho.
- `-c`: Tóm tắt các cuộc gọi hệ thống và thời gian thực hiện của chúng.

## Ví dụ thường gặp
- Theo dõi một chương trình đơn giản:

```bash
strace ls
```

- Ghi đầu ra vào một tập tin:

```bash
strace -o output.txt ls
```

- Theo dõi một tiến trình đang chạy:

```bash
strace -p 1234
```

- Theo dõi chỉ các cuộc gọi liên quan đến tệp:

```bash
strace -e trace=file ls
```

- Tóm tắt các cuộc gọi hệ thống:

```bash
strace -c ls
```

## Mẹo
- Sử dụng tùy chọn `-o` để lưu lại đầu ra cho việc phân tích sau này.
- Kết hợp `strace` với các lệnh khác để theo dõi hành vi của các chương trình phức tạp hơn.
- Đọc kỹ đầu ra để xác định các vấn đề tiềm ẩn trong mã nguồn hoặc cấu hình của ứng dụng.