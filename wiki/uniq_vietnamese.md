# [Hệ điều hành Debian] Debian Almquist Shell (dash) uniq Cách sử dụng: Loại bỏ các dòng trùng lặp

## Overview
Lệnh `uniq` trong shell được sử dụng để loại bỏ các dòng trùng lặp liên tiếp trong một tệp hoặc đầu vào từ dòng lệnh. Nó rất hữu ích khi bạn muốn làm sạch dữ liệu hoặc chỉ giữ lại các dòng duy nhất.

## Usage
Cú pháp cơ bản của lệnh `uniq` như sau:
```
uniq [options] [arguments]
```

## Common Options
- `-c`: Đếm số lần xuất hiện của mỗi dòng.
- `-d`: Chỉ hiển thị các dòng trùng lặp.
- `-u`: Chỉ hiển thị các dòng không trùng lặp.
- `-i`: Bỏ qua sự khác biệt giữa chữ hoa và chữ thường.

## Common Examples
- Loại bỏ các dòng trùng lặp trong một tệp:
  ```bash
  uniq input.txt output.txt
  ```
  
- Đếm số lần xuất hiện của mỗi dòng:
  ```bash
  uniq -c input.txt
  ```

- Chỉ hiển thị các dòng trùng lặp:
  ```bash
  uniq -d input.txt
  ```

- Chỉ hiển thị các dòng không trùng lặp:
  ```bash
  uniq -u input.txt
  ```

- Bỏ qua sự khác biệt giữa chữ hoa và chữ thường:
  ```bash
  uniq -i input.txt output.txt
  ```

## Tips
- Để `uniq` hoạt động chính xác, đầu vào cần phải được sắp xếp. Bạn có thể sử dụng lệnh `sort` trước khi `uniq`.
- Kết hợp `uniq` với `sort` để loại bỏ các dòng trùng lặp trong một tệp:
  ```bash
  sort input.txt | uniq > output.txt
  ```
- Sử dụng các tùy chọn một cách linh hoạt để phù hợp với nhu cầu cụ thể của bạn và tối ưu hóa kết quả đầu ra.