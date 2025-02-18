# [Hệ điều hành] Debian Almquist Shell (dash) hostname sử dụng: [quản lý tên máy]

## Tổng quan
Lệnh `hostname` trong shell Debian Almquist (dash) được sử dụng để hiển thị hoặc thiết lập tên của máy tính. Tên máy tính là một phần quan trọng trong việc xác định và quản lý các thiết bị trong mạng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `hostname` như sau:
```
hostname [options] [arguments]
```

## Các tùy chọn phổ biến
- `-f`, `--fqdn`: Hiển thị tên miền đầy đủ (Fully Qualified Domain Name).
- `-i`, `--ip-address`: Hiển thị địa chỉ IP của máy.
- `-s`, `--short`: Hiển thị tên ngắn của máy.
- `-V`, `--version`: Hiển thị phiên bản của lệnh hostname.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `hostname`:

1. Hiển thị tên máy hiện tại:
   ```bash
   hostname
   ```

2. Hiển thị tên miền đầy đủ:
   ```bash
   hostname -f
   ```

3. Hiển thị địa chỉ IP của máy:
   ```bash
   hostname -i
   ```

4. Thiết lập tên máy mới:
   ```bash
   sudo hostname new-hostname
   ```

5. Hiển thị tên ngắn của máy:
   ```bash
   hostname -s
   ```

## Mẹo
- Để thay đổi tên máy một cách vĩnh viễn, bạn cần chỉnh sửa tệp cấu hình `/etc/hostname`.
- Sau khi thay đổi tên máy, hãy khởi động lại máy hoặc sử dụng lệnh `hostname` để áp dụng thay đổi ngay lập tức.
- Kiểm tra tên máy thường xuyên có thể giúp bạn quản lý mạng hiệu quả hơn, đặc biệt trong môi trường có nhiều thiết bị.