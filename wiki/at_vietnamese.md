# [Hệ điều hành] Debian Almquist Shell (dash) tại at: [lên lịch thực thi lệnh]

## Tổng quan
Lệnh `at` trong shell cho phép người dùng lên lịch thực thi một lệnh hoặc tập lệnh vào một thời điểm cụ thể trong tương lai. Điều này rất hữu ích khi bạn muốn tự động hóa các tác vụ mà không cần phải can thiệp thủ công.

## Cách sử dụng
Cú pháp cơ bản của lệnh `at` như sau:

```
at [options] [arguments]
```

## Các tùy chọn phổ biến
- `-f FILE`: Chỉ định tệp chứa lệnh cần thực thi.
- `-m`: Gửi email thông báo khi lệnh đã được thực thi.
- `-q QUEUE`: Chỉ định hàng đợi để thực thi lệnh.
- `-t TIME`: Chỉ định thời gian cụ thể để thực thi lệnh.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `at`:

1. **Lên lịch thực thi lệnh ngay sau 5 phút:**
   ```bash
   echo "echo 'Hello World'" | at now + 5 minutes
   ```

2. **Lên lịch thực thi một tệp lệnh vào lúc 3 giờ chiều hôm nay:**
   ```bash
   at 15:00 -f /path/to/script.sh
   ```

3. **Lên lịch gửi email thông báo khi lệnh được thực thi:**
   ```bash
   echo "backup.sh" | at now + 1 hour -m
   ```

4. **Lên lịch thực thi vào một ngày cụ thể:**
   ```bash
   echo "shutdown -h now" | at 22:00 2023-10-15
   ```

## Mẹo
- **Kiểm tra các tác vụ đã lên lịch:** Bạn có thể sử dụng lệnh `atq` để xem danh sách các tác vụ đã được lên lịch.
- **Hủy tác vụ đã lên lịch:** Sử dụng lệnh `atrm JOB_ID` để hủy một tác vụ cụ thể mà bạn không còn muốn thực hiện.
- **Sử dụng với cron:** Kết hợp `at` với `cron` có thể giúp bạn lên lịch các tác vụ phức tạp hơn.