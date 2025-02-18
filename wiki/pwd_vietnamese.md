# [Hệ điều hành Debian] Debian Almquist Shell (dash) pwd Cách sử dụng: Xác định thư mục hiện tại

## Tổng quan
Lệnh `pwd` (print working directory) được sử dụng để hiển thị đường dẫn tuyệt đối của thư mục hiện tại mà người dùng đang làm việc trong dòng lệnh. Đây là một công cụ hữu ích để xác định vị trí của bạn trong hệ thống tệp.

## Cách sử dụng
Cú pháp cơ bản của lệnh `pwd` như sau:

```
pwd [options] [arguments]
```

## Các tùy chọn phổ biến
- `-L`: Hiển thị đường dẫn logic (theo liên kết).
- `-P`: Hiển thị đường dẫn vật lý (không theo liên kết).

## Ví dụ thường gặp
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `pwd`:

1. Hiển thị thư mục hiện tại:
   ```sh
   pwd
   ```

2. Hiển thị đường dẫn vật lý:
   ```sh
   pwd -P
   ```

3. Hiển thị đường dẫn logic:
   ```sh
   pwd -L
   ```

## Mẹo
- Sử dụng `pwd` thường xuyên để xác định vị trí của bạn trong hệ thống tệp, đặc biệt khi làm việc với nhiều thư mục.
- Kết hợp lệnh `pwd` với các lệnh khác như `cd` để dễ dàng điều hướng trong hệ thống tệp.
- Nếu bạn đang sử dụng các liên kết mềm, hãy nhớ rằng tùy chọn `-L` sẽ giúp bạn thấy đường dẫn mà bạn đã truy cập thông qua các liên kết đó.