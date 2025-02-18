# [Hệ điều hành] Debian Almquist Shell (dash) netstat Cách sử dụng: Kiểm tra kết nối mạng

## Tổng quan
Lệnh `netstat` được sử dụng để hiển thị thông tin về các kết nối mạng, bảng định tuyến, và các giao thức mạng đang hoạt động trên hệ thống. Đây là một công cụ hữu ích để theo dõi trạng thái mạng và phát hiện các vấn đề liên quan đến kết nối.

## Cách sử dụng
Cú pháp cơ bản của lệnh `netstat` như sau:

```
netstat [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `-a`: Hiển thị tất cả các kết nối và cổng đang lắng nghe.
- `-n`: Hiển thị địa chỉ IP và số cổng thay vì tên miền.
- `-t`: Hiển thị các kết nối TCP.
- `-u`: Hiển thị các kết nối UDP.
- `-l`: Hiển thị các cổng đang lắng nghe.
- `-p`: Hiển thị PID và tên của chương trình đang sử dụng kết nối.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `netstat`:

- Hiển thị tất cả các kết nối và cổng đang lắng nghe:
  ```bash
  netstat -a
  ```

- Hiển thị các kết nối TCP đang hoạt động:
  ```bash
  netstat -t
  ```

- Hiển thị các kết nối UDP:
  ```bash
  netstat -u
  ```

- Hiển thị các cổng đang lắng nghe:
  ```bash
  netstat -l
  ```

- Hiển thị thông tin chi tiết về các kết nối với PID:
  ```bash
  netstat -p
  ```

## Mẹo
- Sử dụng tùy chọn `-n` để tăng tốc độ hiển thị thông tin bằng cách bỏ qua việc phân giải tên miền.
- Kết hợp các tùy chọn để có được thông tin chi tiết hơn, ví dụ: `netstat -tuln` để xem các kết nối TCP và UDP đang lắng nghe mà không phân giải tên miền.
- Để theo dõi các thay đổi theo thời gian, bạn có thể sử dụng lệnh `watch` với `netstat`, ví dụ: `watch netstat -a`.