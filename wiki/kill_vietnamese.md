# [Hệ điều hành] Debian Almquist Shell (dash) kill Cách sử dụng: Dừng tiến trình

## Overview
Lệnh `kill` trong shell được sử dụng để gửi tín hiệu đến một hoặc nhiều tiến trình. Tín hiệu này thường được sử dụng để yêu cầu tiến trình dừng lại hoặc thực hiện một hành động cụ thể.

## Usage
Cú pháp cơ bản của lệnh `kill` như sau:
```
kill [options] [arguments]
```

## Common Options
- `-l`: Liệt kê tất cả các tín hiệu có sẵn.
- `-s SIGNAL`: Gửi tín hiệu cụ thể đến tiến trình.
- `-n NUMBER`: Gửi tín hiệu theo số hiệu tín hiệu.

## Common Examples
- Dừng một tiến trình bằng ID tiến trình (PID):
  ```sh
  kill 1234
  ```
- Gửi tín hiệu `SIGKILL` để buộc dừng một tiến trình:
  ```sh
  kill -9 1234
  ```
- Gửi tín hiệu `SIGTERM` đến một tiến trình cụ thể:
  ```sh
  kill -15 1234
  ```
- Liệt kê tất cả các tín hiệu có sẵn:
  ```sh
  kill -l
  ```

## Tips
- Luôn kiểm tra PID của tiến trình trước khi sử dụng lệnh `kill` để tránh dừng nhầm tiến trình quan trọng.
- Sử dụng tín hiệu `SIGTERM` (mặc định) trước khi sử dụng `SIGKILL`, vì `SIGTERM` cho phép tiến trình thực hiện các thao tác dọn dẹp.
- Bạn có thể sử dụng lệnh `ps` để tìm PID của tiến trình mà bạn muốn dừng.