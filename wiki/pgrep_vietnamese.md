# [Hệ điều hành] Debian Almquist Shell (dash) pgrep: Tìm kiếm PID của tiến trình

## Overview
Lệnh `pgrep` được sử dụng để tìm kiếm và liệt kê các ID tiến trình (PID) của các tiến trình đang chạy trên hệ thống, dựa trên tên hoặc các thuộc tính khác của tiến trình.

## Usage
Cú pháp cơ bản của lệnh `pgrep` như sau:
```
pgrep [options] [arguments]
```

## Common Options
- `-u, --euid`: Tìm kiếm các tiến trình của người dùng cụ thể.
- `-n, --newest`: Chỉ hiển thị PID của tiến trình mới nhất.
- `-o, --oldest`: Chỉ hiển thị PID của tiến trình cũ nhất.
- `-f, --full`: Tìm kiếm theo toàn bộ dòng lệnh, không chỉ tên tiến trình.

## Common Examples
- Tìm PID của tiến trình có tên là `bash`:
  ```sh
  pgrep bash
  ```

- Tìm PID của tiến trình do người dùng `user1` sở hữu:
  ```sh
  pgrep -u user1
  ```

- Tìm PID của tiến trình mới nhất có tên là `python`:
  ```sh
  pgrep -n python
  ```

- Tìm PID của tiến trình cũ nhất có tên là `nginx`:
  ```sh
  pgrep -o nginx
  ```

- Tìm PID của tiến trình dựa trên toàn bộ dòng lệnh:
  ```sh
  pgrep -f "python script.py"
  ```

## Tips
- Sử dụng `pgrep` trong các script để tự động hóa việc theo dõi tiến trình.
- Kết hợp `pgrep` với lệnh `kill` để dừng các tiến trình cụ thể:
  ```sh
  kill $(pgrep process_name)
  ```
- Kiểm tra tài liệu bằng cách sử dụng `man pgrep` để biết thêm thông tin chi tiết về các tùy chọn và cách sử dụng.