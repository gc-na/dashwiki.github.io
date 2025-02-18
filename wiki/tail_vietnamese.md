# [Hệ điều hành Debian] Debian Almquist Shell (dash) tail Cách sử dụng: Xem nội dung cuối của tệp

## Tổng quan
Lệnh `tail` trong shell được sử dụng để hiển thị các dòng cuối cùng của một tệp. Đây là công cụ hữu ích để theo dõi các tệp log hoặc kiểm tra nội dung mới được thêm vào.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tail` như sau:
```
tail [options] [arguments]
```

## Các tùy chọn phổ biến
- `-n [số]`: Hiển thị số dòng cuối cùng được chỉ định từ tệp.
- `-f`: Theo dõi tệp và hiển thị các dòng mới khi chúng được thêm vào.
- `-c [số]`: Hiển thị số byte cuối cùng được chỉ định từ tệp.

## Ví dụ phổ biến
- Hiển thị 10 dòng cuối cùng của tệp `example.txt`:
  ```sh
  tail example.txt
  ```

- Hiển thị 20 dòng cuối cùng của tệp `logfile.log`:
  ```sh
  tail -n 20 logfile.log
  ```

- Theo dõi tệp `access.log` để xem các dòng mới được thêm vào:
  ```sh
  tail -f access.log
  ```

- Hiển thị 50 byte cuối cùng của tệp `data.txt`:
  ```sh
  tail -c 50 data.txt
  ```

## Mẹo
- Sử dụng tùy chọn `-f` để theo dõi các tệp log trong thời gian thực, điều này rất hữu ích khi bạn muốn giám sát hoạt động của hệ thống.
- Kết hợp `tail` với `grep` để lọc các dòng cụ thể trong tệp log:
  ```sh
  tail -f logfile.log | grep "ERROR"
  ```
- Nếu bạn muốn xem nội dung của nhiều tệp cùng lúc, bạn có thể chỉ định nhiều tệp trong lệnh `tail`:
  ```sh
  tail file1.txt file2.txt
  ```