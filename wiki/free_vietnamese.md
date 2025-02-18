# [Hệ điều hành] Debian Almquist Shell (dash) free: Kiểm tra bộ nhớ hệ thống

## Overview
Lệnh `free` trong shell (dash) được sử dụng để hiển thị thông tin về bộ nhớ hệ thống, bao gồm bộ nhớ vật lý, bộ nhớ swap và bộ nhớ cache. Nó giúp người dùng theo dõi tình trạng sử dụng bộ nhớ trong thời gian thực.

## Usage
Cú pháp cơ bản của lệnh `free` như sau:
```
free [options] [arguments]
```

## Common Options
- `-h`: Hiển thị kích thước bộ nhớ theo định dạng dễ đọc (KB, MB, GB).
- `-m`: Hiển thị thông tin bộ nhớ theo megabyte.
- `-g`: Hiển thị thông tin bộ nhớ theo gigabyte.
- `-s <seconds>`: Cập nhật thông tin sau mỗi khoảng thời gian nhất định (tính bằng giây).
- `-t`: Hiển thị tổng số bộ nhớ sử dụng và còn lại.

## Common Examples
Dưới đây là một số ví dụ thực tế khi sử dụng lệnh `free`:

1. Hiển thị thông tin bộ nhớ mặc định:
   ```bash
   free
   ```

2. Hiển thị thông tin bộ nhớ theo định dạng dễ đọc:
   ```bash
   free -h
   ```

3. Hiển thị thông tin bộ nhớ theo megabyte:
   ```bash
   free -m
   ```

4. Cập nhật thông tin bộ nhớ mỗi 5 giây:
   ```bash
   free -s 5
   ```

5. Hiển thị tổng số bộ nhớ sử dụng và còn lại:
   ```bash
   free -t
   ```

## Tips
- Sử dụng tùy chọn `-h` để dễ dàng đọc và hiểu thông tin bộ nhớ.
- Kết hợp lệnh `free` với lệnh `watch` để theo dõi tình trạng bộ nhớ theo thời gian thực:
  ```bash
  watch free -h
  ```
- Thường xuyên kiểm tra bộ nhớ để phát hiện sớm các vấn đề về hiệu suất hệ thống.