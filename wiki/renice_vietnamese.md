# [Hệ điều hành] Debian Almquist Shell (dash) renice: Thay đổi ưu tiên của tiến trình

## Tổng quan
Lệnh `renice` được sử dụng để thay đổi mức độ ưu tiên của một hoặc nhiều tiến trình đang chạy trên hệ thống. Mức độ ưu tiên này ảnh hưởng đến cách mà hệ thống phân bổ tài nguyên cho các tiến trình, giúp cải thiện hiệu suất của các ứng dụng quan trọng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `renice` như sau:
```
renice [options] [arguments]
```

## Các tùy chọn phổ biến
- `-n, --priority <giá trị>`: Chỉ định mức độ ưu tiên mới cho tiến trình. Giá trị có thể là một số nguyên từ -20 (ưu tiên cao nhất) đến 19 (ưu tiên thấp nhất).
- `-p, --pid <pid>`: Chỉ định ID tiến trình (PID) mà bạn muốn thay đổi mức độ ưu tiên.
- `-g, --pgroup <pgid>`: Chỉ định nhóm tiến trình mà bạn muốn thay đổi mức độ ưu tiên.
- `-u, --user <tên người dùng>`: Chỉ định tiến trình của một người dùng cụ thể.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `renice`:

1. Thay đổi mức độ ưu tiên của một tiến trình với PID 1234 thành 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Thay đổi mức độ ưu tiên cho tất cả các tiến trình của người dùng "user1" thành -5:
   ```bash
   renice -n -5 -u user1
   ```

3. Thay đổi mức độ ưu tiên cho nhóm tiến trình với PGID 5678 thành 0:
   ```bash
   renice -n 0 -g 5678
   ```

## Mẹo
- Trước khi thay đổi mức độ ưu tiên, hãy kiểm tra mức độ ưu tiên hiện tại của tiến trình bằng lệnh `ps -o pid,ni,cmd`.
- Sử dụng mức độ ưu tiên cao (số âm) cho các tiến trình quan trọng để đảm bảo chúng nhận được tài nguyên cần thiết.
- Hãy cẩn thận khi thay đổi mức độ ưu tiên của các tiến trình hệ thống, vì điều này có thể ảnh hưởng đến sự ổn định của hệ thống.