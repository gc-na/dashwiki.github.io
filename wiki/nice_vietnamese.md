# [Hệ điều hành Debian] Debian Almquist Shell (dash) nice: Thay đổi độ ưu tiên của tiến trình

## Tổng quan
Lệnh `nice` trong shell giúp thay đổi độ ưu tiên của một tiến trình khi nó được khởi động. Điều này cho phép người dùng điều chỉnh mức độ ưu tiên của các tiến trình, từ đó ảnh hưởng đến cách mà hệ thống phân bổ tài nguyên cho chúng.

## Cách sử dụng
Cú pháp cơ bản của lệnh `nice` như sau:
```
nice [options] [arguments]
```

## Các tùy chọn thông dụng
- `-n, --adjustment=N`: Điều chỉnh độ ưu tiên của tiến trình. Giá trị N có thể là số dương hoặc âm.
- `-h, --help`: Hiển thị thông tin trợ giúp về lệnh.
- `--version`: Hiển thị phiên bản của lệnh.

## Ví dụ thông dụng
Dưới đây là một số ví dụ về cách sử dụng lệnh `nice`:

1. Khởi động một tiến trình với độ ưu tiên thấp hơn:
   ```sh
   nice -n 10 my_program
   ```

2. Khởi động một tiến trình với độ ưu tiên cao hơn:
   ```sh
   nice -n -5 my_program
   ```

3. Kiểm tra độ ưu tiên của một tiến trình đang chạy:
   ```sh
   ps -o pid,ni,comm
   ```

4. Sử dụng `nice` để chạy một lệnh trong nền với độ ưu tiên thấp:
   ```sh
   nice -n 15 sleep 60 &
   ```

## Mẹo
- Sử dụng `nice` để đảm bảo rằng các tiến trình không chiếm quá nhiều tài nguyên hệ thống, đặc biệt là khi chạy các tác vụ nặng.
- Kiểm tra độ ưu tiên của các tiến trình đang chạy bằng lệnh `ps` để có cái nhìn tổng quan về việc phân bổ tài nguyên.
- Hãy cẩn thận khi điều chỉnh độ ưu tiên cao hơn cho các tiến trình quan trọng, vì điều này có thể làm ảnh hưởng đến hiệu suất của hệ thống.