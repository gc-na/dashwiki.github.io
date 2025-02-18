# [Hệ điều hành Debian] Debian Almquist Shell (dash) dstat: Theo dõi hiệu suất hệ thống

## Tổng quan
Lệnh `dstat` là một công cụ mạnh mẽ dùng để theo dõi hiệu suất hệ thống trong thời gian thực. Nó kết hợp các tính năng của nhiều công cụ khác nhau như `vmstat`, `iostat`, và `netstat`, giúp người dùng có cái nhìn tổng quát về hoạt động của hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `dstat` như sau:
```
dstat [options] [arguments]
```

## Các tùy chọn phổ biến
- `-c`: Hiển thị thông tin về CPU.
- `-d`: Hiển thị thông tin về đĩa.
- `-n`: Hiển thị thông tin về mạng.
- `-r`: Hiển thị thông tin về bộ nhớ.
- `-t`: Hiển thị thời gian.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `dstat`:

1. Hiển thị thông tin về CPU và đĩa:
   ```bash
   dstat -cd
   ```

2. Theo dõi thông tin mạng và bộ nhớ:
   ```bash
   dstat -n -r
   ```

3. Hiển thị tất cả thông tin cùng một lúc:
   ```bash
   dstat -cdrnt
   ```

4. Ghi lại thông tin vào file để phân tích sau:
   ```bash
   dstat -cd --output dstat_output.csv
   ```

## Mẹo
- Sử dụng `dstat` với tùy chọn `--help` để xem danh sách đầy đủ các tùy chọn có sẵn.
- Kết hợp nhiều tùy chọn để có cái nhìn toàn diện hơn về hiệu suất hệ thống.
- Thực hiện lệnh `dstat` trong một phiên terminal riêng biệt để dễ dàng theo dõi mà không làm gián đoạn các tác vụ khác.