# [Hệ điều hành] Debian Almquist Shell (dash) uname Cách sử dụng: Hiển thị thông tin hệ thống

## Tổng quan
Lệnh `uname` trong shell (dash) được sử dụng để hiển thị thông tin về hệ thống đang chạy, bao gồm tên hệ điều hành, tên máy, phiên bản, và nhiều thông tin khác liên quan đến hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `uname` như sau:

```
uname [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-a`: Hiển thị tất cả thông tin hệ thống.
- `-s`: Hiển thị tên hệ điều hành.
- `-n`: Hiển thị tên máy.
- `-r`: Hiển thị phiên bản của hệ điều hành.
- `-v`: Hiển thị thông tin phiên bản.

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `uname`:

1. Hiển thị tất cả thông tin hệ thống:
   ```bash
   uname -a
   ```

2. Hiển thị tên hệ điều hành:
   ```bash
   uname -s
   ```

3. Hiển thị tên máy:
   ```bash
   uname -n
   ```

4. Hiển thị phiên bản của hệ điều hành:
   ```bash
   uname -r
   ```

5. Hiển thị thông tin phiên bản:
   ```bash
   uname -v
   ```

## Mẹo
- Sử dụng `uname -a` để có cái nhìn tổng quan nhất về hệ thống của bạn.
- Kết hợp lệnh `uname` với các lệnh khác trong shell để tự động hóa các tác vụ liên quan đến quản lý hệ thống.
- Nếu bạn chỉ cần một thông tin cụ thể, hãy sử dụng các tùy chọn riêng lẻ để tiết kiệm thời gian và tài nguyên.