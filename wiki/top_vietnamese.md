# [Hệ điều hành] Debian Almquist Shell (dash) top: [giám sát tài nguyên hệ thống]

## Overview
Lệnh `top` trong shell là một công cụ mạnh mẽ dùng để giám sát các tiến trình đang chạy trên hệ thống. Nó cung cấp thông tin thời gian thực về việc sử dụng CPU, bộ nhớ, và các tài nguyên khác của hệ thống, giúp người dùng theo dõi hiệu suất và quản lý các tiến trình.

## Usage
Cú pháp cơ bản của lệnh `top` như sau:
```
top [options] [arguments]
```

## Common Options
- `-d <seconds>`: Đặt thời gian làm mới giữa các lần hiển thị, tính bằng giây.
- `-n <number>`: Chỉ định số lần cập nhật trước khi thoát.
- `-b`: Chạy `top` trong chế độ batch, thích hợp cho việc ghi lại thông tin.
- `-u <username>`: Hiển thị chỉ các tiến trình của người dùng cụ thể.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `top`:

1. Chạy `top` với cập nhật mỗi 5 giây:
   ```bash
   top -d 5
   ```

2. Chạy `top` và chỉ hiển thị tiến trình của người dùng "john":
   ```bash
   top -u john
   ```

3. Chạy `top` trong chế độ batch và ghi kết quả vào file:
   ```bash
   top -b -n 1 > output.txt
   ```

4. Chạy `top` và thoát sau 10 lần cập nhật:
   ```bash
   top -n 10
   ```

## Tips
- Sử dụng phím `h` trong giao diện `top` để xem hướng dẫn sử dụng nhanh.
- Nhấn `Shift + M` để sắp xếp các tiến trình theo mức sử dụng bộ nhớ.
- Nhấn `q` để thoát khỏi giao diện `top` khi không còn cần thiết.