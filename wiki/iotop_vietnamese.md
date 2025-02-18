# [Hệ điều hành Debian] Debian Almquist Shell (dash) iotop: Theo dõi hoạt động I/O của các tiến trình

## Tổng quan
Lệnh `iotop` được sử dụng để theo dõi hoạt động I/O (Input/Output) của các tiến trình đang chạy trên hệ thống. Nó cho phép người dùng xem các tiến trình nào đang sử dụng tài nguyên đĩa nhiều nhất, từ đó giúp chẩn đoán các vấn đề về hiệu suất.

## Cách sử dụng
Cú pháp cơ bản của lệnh `iotop` như sau:

```
iotop [options] [arguments]
```

## Các tùy chọn phổ biến
- `-o`, `--only`: Chỉ hiển thị các tiến trình đang thực hiện hoạt động I/O.
- `-b`, `--batch`: Chạy trong chế độ batch, thích hợp cho việc ghi lại đầu ra vào tệp.
- `-n NUM`, `--iter NUM`: Chỉ định số lần cập nhật thông tin trước khi thoát.
- `-d SEC`, `--delay SEC`: Thay đổi thời gian giữa các lần cập nhật thông tin, tính bằng giây.

## Ví dụ thường gặp
- Để khởi động `iotop` và xem tất cả các tiến trình đang sử dụng I/O:
  ```bash
  iotop
  ```

- Để chỉ hiển thị các tiến trình đang hoạt động I/O:
  ```bash
  iotop -o
  ```

- Để chạy `iotop` trong chế độ batch và ghi đầu ra vào tệp:
  ```bash
  iotop -b -n 10 > output.txt
  ```

- Để thay đổi thời gian giữa các lần cập nhật thông tin thành 2 giây:
  ```bash
  iotop -d 2
  ```

## Mẹo
- Sử dụng tùy chọn `-o` để chỉ xem các tiến trình đang hoạt động, giúp bạn dễ dàng xác định vấn đề.
- Khi chạy trong chế độ batch, bạn có thể ghi lại đầu ra để phân tích sau này.
- Thường xuyên theo dõi I/O có thể giúp bạn phát hiện các tiến trình không hiệu quả hoặc các vấn đề về đĩa sớm hơn.