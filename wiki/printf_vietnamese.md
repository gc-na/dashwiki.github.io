# [Hệ điều hành] Debian Almquist Shell (dash) printf Cách sử dụng: In định dạng văn bản

## Overview
Lệnh `printf` trong shell dash được sử dụng để định dạng và in ra văn bản. Nó cho phép người dùng kiểm soát cách mà dữ liệu được hiển thị, bao gồm cả việc định dạng số, chuỗi và các ký tự đặc biệt.

## Usage
Cú pháp cơ bản của lệnh `printf` như sau:
```sh
printf [options] [arguments]
```

## Common Options
- `-v var`: Gán kết quả vào biến `var` thay vì in ra.
- `--help`: Hiển thị thông tin trợ giúp về lệnh `printf`.
- `--version`: Hiển thị phiên bản của lệnh `printf`.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `printf`:

1. In một chuỗi đơn giản:
   ```sh
   printf "Hello, World!\n"
   ```

2. Định dạng số nguyên:
   ```sh
   printf "Số nguyên: %d\n" 42
   ```

3. Định dạng số thực:
   ```sh
   printf "Số thực: %.2f\n" 3.14159
   ```

4. In nhiều biến:
   ```sh
   name="Alice"
   age=30
   printf "%s is %d years old.\n" "$name" "$age"
   ```

5. Sử dụng gán vào biến:
   ```sh
   result=$(printf "Tổng: %d\n" 100)
   printf "$result"
   ```

## Tips
- Sử dụng `\n` để thêm dòng mới trong chuỗi in ra.
- Kiểm tra kỹ định dạng để đảm bảo kết quả hiển thị đúng như mong muốn.
- Hãy nhớ rằng `printf` không tự động thêm dòng mới như lệnh `echo`, vì vậy bạn cần phải thêm `\n` nếu cần.