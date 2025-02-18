# [Hệ điều hành Linux] Debian Almquist Shell (dash) nohup: Chạy lệnh không bị ngắt kết nối

## Overview
Lệnh `nohup` (no hang up) cho phép bạn chạy một lệnh trong nền mà không bị ngắt kết nối khi bạn đăng xuất khỏi phiên làm việc. Điều này rất hữu ích khi bạn muốn thực hiện các tác vụ dài mà không cần phải giữ phiên mở.

## Usage
Cú pháp cơ bản của lệnh `nohup` như sau:
```
nohup [options] [arguments]
```

## Common Options
- `&`: Chạy lệnh trong nền.
- `-h`: Hiển thị thông tin trợ giúp về lệnh `nohup`.
- `-v`: Hiển thị phiên bản của `nohup`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `nohup`:

1. Chạy một script trong nền:
   ```bash
   nohup ./my_script.sh &
   ```

2. Chạy một lệnh dài và ghi đầu ra vào file `nohup.out`:
   ```bash
   nohup long_running_command > output.log &
   ```

3. Chạy một lệnh với đầu ra cả lỗi và thông báo:
   ```bash
   nohup command_name > output.log 2>&1 &
   ```

4. Chạy một lệnh Python trong nền:
   ```bash
   nohup python my_script.py &
   ```

## Tips
- Luôn kiểm tra file `nohup.out` để xem đầu ra của lệnh đã chạy.
- Sử dụng `&` để đảm bảo lệnh chạy trong nền, giúp bạn tiếp tục sử dụng terminal.
- Nếu bạn muốn chạy lệnh mà không ghi đè lên file `nohup.out`, hãy chỉ định một file khác cho đầu ra.