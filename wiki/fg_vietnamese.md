# [Hệ điều hành] Debian Almquist Shell (dash) fg <Sử dụng tương đương>: Chuyển tiếp tiến trình nền lên nền trước

## Tổng quan
Lệnh `fg` trong shell của Debian Almquist (dash) được sử dụng để chuyển một tiến trình đang chạy ở chế độ nền (background) trở lại chế độ nền trước (foreground). Điều này cho phép người dùng tương tác trực tiếp với tiến trình đó.

## Cách sử dụng
Cú pháp cơ bản của lệnh `fg` như sau:
```
fg [options] [job_spec]
```

## Tùy chọn phổ biến
- `job_spec`: Chỉ định tiến trình nào sẽ được chuyển về chế độ foreground. Nếu không có tham số này, tiến trình cuối cùng sẽ được chọn mặc định.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `fg`:

1. Chuyển tiến trình nền cuối cùng về foreground:
   ```sh
   fg
   ```

2. Chuyển một tiến trình cụ thể (ví dụ, tiến trình số 1) về foreground:
   ```sh
   fg %1
   ```

3. Nếu bạn có nhiều tiến trình đang chạy, bạn có thể liệt kê chúng bằng lệnh `jobs` và sau đó chuyển một trong số chúng về foreground:
   ```sh
   jobs
   fg %2
   ```

## Mẹo
- Hãy chắc chắn rằng bạn đã sử dụng lệnh `bg` để đưa tiến trình vào chế độ nền trước khi sử dụng `fg`.
- Sử dụng lệnh `jobs` để kiểm tra trạng thái của các tiến trình nền trước khi chuyển chúng về foreground.
- Nếu bạn cần dừng một tiến trình đang chạy trong foreground, bạn có thể sử dụng tổ hợp phím `Ctrl + Z` để tạm dừng nó và sau đó sử dụng `fg` để tiếp tục.