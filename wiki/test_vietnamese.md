# [Hệ điều hành] Debian Almquist Shell (dash) test: Kiểm tra điều kiện

## Overview
Lệnh `test` trong shell dash được sử dụng để kiểm tra các điều kiện khác nhau, như kiểm tra sự tồn tại của tệp, so sánh số, hoặc kiểm tra chuỗi. Kết quả của lệnh sẽ trả về giá trị đúng (0) hoặc sai (1) tùy thuộc vào điều kiện được kiểm tra.

## Usage
Cú pháp cơ bản của lệnh `test` như sau:
```
test [options] [arguments]
```

## Common Options
- `-e`: Kiểm tra xem tệp có tồn tại hay không.
- `-f`: Kiểm tra xem tệp có phải là tệp thông thường hay không.
- `-d`: Kiểm tra xem tệp có phải là thư mục hay không.
- `-z`: Kiểm tra xem chuỗi có rỗng hay không.
- `-eq`: So sánh hai số xem có bằng nhau hay không.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `test`:

1. Kiểm tra sự tồn tại của một tệp:
   ```sh
   test -e filename.txt && echo "Tệp tồn tại"
   ```

2. Kiểm tra xem một tệp có phải là tệp thông thường:
   ```sh
   test -f filename.txt && echo "Đây là tệp thông thường"
   ```

3. Kiểm tra xem một thư mục có tồn tại hay không:
   ```sh
   test -d /path/to/directory && echo "Thư mục tồn tại"
   ```

4. Kiểm tra xem một chuỗi có rỗng hay không:
   ```sh
   my_string=""
   test -z "$my_string" && echo "Chuỗi rỗng"
   ```

5. So sánh hai số:
   ```sh
   a=5
   b=10
   test $a -eq $b && echo "Hai số bằng nhau" || echo "Hai số khác nhau"
   ```

## Tips
- Sử dụng `&&` và `||` để kết hợp các điều kiện và thực hiện các hành động khác nhau dựa trên kết quả của lệnh `test`.
- Đặt các biến trong dấu ngoặc kép để tránh lỗi khi biến rỗng hoặc có khoảng trắng.
- Lệnh `test` có thể được thay thế bằng dấu ngoặc vuông `[` và `]`, ví dụ: `[ -e filename.txt ]`.