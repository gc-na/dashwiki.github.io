# [Hệ điều hành] Debian Almquist Shell (dash) killall: [dừng tất cả tiến trình]

## Overview
Lệnh `killall` được sử dụng để dừng tất cả các tiến trình đang chạy theo tên. Điều này rất hữu ích khi bạn muốn kết thúc nhiều tiến trình cùng một lúc mà không cần phải tìm kiếm từng tiến trình riêng lẻ.

## Usage
Cú pháp cơ bản của lệnh `killall` như sau:
```
killall [options] [arguments]
```

## Common Options
- `-u <user>`: Chỉ dừng các tiến trình của người dùng cụ thể.
- `-s <signal>`: Gửi tín hiệu cụ thể đến các tiến trình (mặc định là SIGTERM).
- `-q`: Không hiển thị thông báo lỗi nếu không tìm thấy tiến trình.
- `-I`: So sánh tên tiến trình không phân biệt chữ hoa chữ thường.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `killall`:

1. Dừng tất cả các tiến trình có tên `firefox`:
   ```bash
   killall firefox
   ```

2. Dừng tất cả các tiến trình của người dùng `john`:
   ```bash
   killall -u john
   ```

3. Gửi tín hiệu SIGKILL đến tất cả các tiến trình có tên `myapp`:
   ```bash
   killall -s SIGKILL myapp
   ```

4. Dừng tất cả các tiến trình `python` mà không phân biệt chữ hoa chữ thường:
   ```bash
   killall -I python
   ```

5. Dừng tất cả các tiến trình mà không hiển thị thông báo lỗi:
   ```bash
   killall -q someprocess
   ```

## Tips
- Hãy cẩn thận khi sử dụng `killall`, vì nó sẽ dừng tất cả các tiến trình có tên giống nhau mà không hỏi xác nhận.
- Sử dụng tùy chọn `-q` để tránh thông báo lỗi không cần thiết khi không tìm thấy tiến trình.
- Nếu bạn không chắc chắn về tiến trình nào đang chạy, hãy sử dụng lệnh `ps` để kiểm tra trước khi sử dụng `killall`.