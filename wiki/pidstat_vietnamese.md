# [Hệ điều hành] Debian Almquist Shell (dash) pidstat Cách sử dụng: Theo dõi thông tin tiến trình

## Tổng quan
Lệnh `pidstat` là một công cụ hữu ích trong việc theo dõi và báo cáo thông tin về việc sử dụng CPU và các tài nguyên khác của các tiến trình đang chạy trên hệ thống. Nó giúp người dùng phân tích hiệu suất của các tiến trình và xác định các vấn đề tiềm ẩn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `pidstat` như sau:
```bash
pidstat [options] [arguments]
```

## Các tùy chọn phổ biến
- `-h`: Hiển thị tiêu đề cho các cột.
- `-r`: Hiển thị thông tin về việc sử dụng bộ nhớ.
- `-u`: Hiển thị thông tin về việc sử dụng CPU.
- `-p <pid>`: Theo dõi một tiến trình cụ thể bằng cách chỉ định PID.
- `-t`: Hiển thị thông tin cho tất cả các luồng của tiến trình.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `pidstat`:

1. Theo dõi việc sử dụng CPU của tất cả các tiến trình:
   ```bash
   pidstat
   ```

2. Theo dõi việc sử dụng CPU của một tiến trình cụ thể với PID 1234:
   ```bash
   pidstat -p 1234
   ```

3. Hiển thị thông tin về việc sử dụng bộ nhớ:
   ```bash
   pidstat -r
   ```

4. Theo dõi tất cả các luồng của một tiến trình cụ thể:
   ```bash
   pidstat -t -p 1234
   ```

5. Hiển thị thông tin theo định kỳ mỗi 2 giây:
   ```bash
   pidstat 2
   ```

## Mẹo
- Sử dụng tùy chọn `-h` để dễ dàng đọc tiêu đề cột trong kết quả.
- Kết hợp `pidstat` với các lệnh khác như `grep` để lọc thông tin theo nhu cầu.
- Theo dõi thường xuyên các tiến trình quan trọng để phát hiện sớm các vấn đề hiệu suất.