# [Hệ điều hành] Debian Almquist Shell (dash) cal <Sử dụng tương đương>: Hiển thị lịch

## Tổng quan
Lệnh `cal` được sử dụng để hiển thị lịch tháng hoặc năm trong dòng lệnh. Nó cho phép người dùng xem các ngày trong tháng cụ thể hoặc toàn bộ năm, giúp dễ dàng theo dõi các sự kiện và ngày quan trọng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `cal` như sau:
```
cal [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `-m`: Hiển thị tháng hiện tại.
- `-y`: Hiển thị lịch cho toàn bộ năm hiện tại.
- `-3`: Hiển thị tháng trước, tháng hiện tại và tháng tiếp theo.
- `-j`: Hiển thị số ngày trong năm (Julian calendar).
- `-A [số]`: Hiển thị số tháng sau tháng hiện tại.
- `-B [số]`: Hiển thị số tháng trước tháng hiện tại.

## Ví dụ phổ biến
- Hiển thị lịch tháng hiện tại:
  ```bash
  cal
  ```

- Hiển thị lịch cho tháng 12 năm 2023:
  ```bash
  cal 12 2023
  ```

- Hiển thị lịch cho toàn bộ năm 2023:
  ```bash
  cal -y 2023
  ```

- Hiển thị lịch cho tháng hiện tại cùng với tháng trước và tháng tiếp theo:
  ```bash
  cal -3
  ```

- Hiển thị lịch với số ngày trong năm:
  ```bash
  cal -j
  ```

## Mẹo
- Sử dụng tùy chọn `-A` và `-B` để dễ dàng xem lịch cho các tháng liền kề mà không cần phải nhập lại lệnh.
- Kết hợp `cal` với `grep` để tìm kiếm các ngày cụ thể trong tháng.
- Thêm lệnh `cal` vào script để tự động gửi thông báo về các sự kiện quan trọng dựa trên lịch.