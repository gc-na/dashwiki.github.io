# [Hệ điều hành] Debian Almquist Shell (dash) traceroute: [theo dõi đường đi của gói tin]

## Tổng quan
Lệnh `traceroute` được sử dụng để theo dõi đường đi của gói tin từ máy tính của bạn đến một địa chỉ IP hoặc tên miền cụ thể. Nó cho phép bạn xác định các điểm dừng (hop) mà gói tin đi qua trên đường đến đích, giúp bạn phân tích và khắc phục sự cố mạng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `traceroute` như sau:

```bash
traceroute [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-m <số>`: Xác định số lượng hop tối đa mà traceroute sẽ theo dõi.
- `-n`: Hiển thị địa chỉ IP thay vì tên miền.
- `-w <giây>`: Đặt thời gian chờ cho mỗi gói tin.
- `-q <số>`: Số lượng gói tin sẽ được gửi đến mỗi hop.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `traceroute`:

1. Theo dõi đường đi đến một địa chỉ IP:
   ```bash
   traceroute 8.8.8.8
   ```

2. Theo dõi đường đi đến một tên miền:
   ```bash
   traceroute www.google.com
   ```

3. Sử dụng tùy chọn `-n` để hiển thị địa chỉ IP:
   ```bash
   traceroute -n www.google.com
   ```

4. Đặt số lượng hop tối đa là 15:
   ```bash
   traceroute -m 15 www.google.com
   ```

## Mẹo
- Sử dụng tùy chọn `-n` để tăng tốc độ thực hiện lệnh, vì nó sẽ không thực hiện phân giải tên miền.
- Kiểm tra các hop để xác định vị trí có thể xảy ra sự cố mạng.
- Nếu bạn gặp phải vấn đề với một địa chỉ cụ thể, hãy thử sử dụng `traceroute` với các tùy chọn khác nhau để có cái nhìn rõ hơn về vấn đề.