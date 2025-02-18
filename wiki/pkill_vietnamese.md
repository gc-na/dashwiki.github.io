# [Hệ điều hành] Debian Almquist Shell (dash) pkill: [kết thúc tiến trình theo tên]

## Tổng quan
Lệnh `pkill` trong shell Debian Almquist (dash) được sử dụng để kết thúc các tiến trình đang chạy dựa trên tên của chúng. Điều này giúp người dùng dễ dàng quản lý và dọn dẹp các tiến trình không cần thiết mà không cần phải tìm kiếm ID tiến trình (PID).

## Cách sử dụng
Cú pháp cơ bản của lệnh `pkill` như sau:

```bash
pkill [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-f`: Tìm kiếm tên tiến trình trong toàn bộ dòng lệnh.
- `-n`: Kết thúc tiến trình mới nhất (mới nhất theo thời gian).
- `-o`: Kết thúc tiến trình cũ nhất (cũ nhất theo thời gian).
- `-signal`: Gửi tín hiệu cụ thể đến tiến trình (mặc định là SIGTERM).

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `pkill`:

1. Kết thúc tất cả các tiến trình có tên "firefox":
   ```bash
   pkill firefox
   ```

2. Kết thúc tiến trình "python" với tín hiệu SIGKILL:
   ```bash
   pkill -9 python
   ```

3. Kết thúc tiến trình mới nhất có tên "chrome":
   ```bash
   pkill -n chrome
   ```

4. Kết thúc tất cả các tiến trình chứa từ "server" trong dòng lệnh:
   ```bash
   pkill -f server
   ```

## Mẹo
- Sử dụng tùy chọn `-l` để liệt kê tất cả các tín hiệu có sẵn mà bạn có thể gửi đến tiến trình.
- Hãy cẩn thận khi sử dụng `pkill`, vì nó có thể kết thúc nhiều tiến trình cùng lúc nếu chúng có tên giống nhau.
- Kiểm tra trước các tiến trình sẽ bị ảnh hưởng bằng cách sử dụng lệnh `pgrep` với cùng các tùy chọn trước khi thực hiện `pkill`.