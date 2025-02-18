# [Hệ điều hành] Debian Almquist Shell (dash) whoami: [hiển thị tên người dùng hiện tại]

## Tổng quan
Lệnh `whoami` trong shell cho phép bạn xác định tên người dùng hiện tại mà bạn đang đăng nhập. Đây là một công cụ hữu ích để kiểm tra danh tính người dùng trong môi trường dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `whoami` như sau:

```bash
whoami [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `--help`: Hiển thị thông tin trợ giúp về lệnh `whoami`.
- `--version`: Hiển thị phiên bản của lệnh `whoami`.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `whoami`:

1. Hiển thị tên người dùng hiện tại:
   ```bash
   whoami
   ```

2. Hiển thị thông tin trợ giúp:
   ```bash
   whoami --help
   ```

3. Kiểm tra phiên bản của lệnh:
   ```bash
   whoami --version
   ```

## Mẹo
- Sử dụng `whoami` khi bạn cần xác minh danh tính người dùng trong các script hoặc khi làm việc với nhiều tài khoản người dùng.
- Kết hợp `whoami` với các lệnh khác để tạo ra các script tự động hóa hiệu quả hơn.