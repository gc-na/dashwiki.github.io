# [Hệ điều hành] Debian Almquist Shell (dash) wc Cách sử dụng: Đếm số dòng, từ và ký tự trong tệp

## Tổng quan
Lệnh `wc` (word count) trong shell được sử dụng để đếm số dòng, số từ và số ký tự trong một hoặc nhiều tệp. Đây là một công cụ hữu ích để phân tích nội dung của tệp văn bản.

## Cách sử dụng
Cú pháp cơ bản của lệnh `wc` như sau:
```bash
wc [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-l`: Đếm số dòng.
- `-w`: Đếm số từ.
- `-c`: Đếm số ký tự.
- `-m`: Đếm số ký tự (bao gồm cả ký tự Unicode).
- `-L`: Hiển thị độ dài của dòng dài nhất.

## Ví dụ phổ biến
1. Đếm số dòng trong một tệp:
   ```bash
   wc -l ten_tap.txt
   ```

2. Đếm số từ trong một tệp:
   ```bash
   wc -w ten_tap.txt
   ```

3. Đếm số ký tự trong một tệp:
   ```bash
   wc -c ten_tap.txt
   ```

4. Đếm số dòng, số từ và số ký tự cùng một lúc:
   ```bash
   wc ten_tap.txt
   ```

5. Đếm số ký tự trong nhiều tệp:
   ```bash
   wc -c tap1.txt tap2.txt
   ```

## Mẹo
- Bạn có thể kết hợp nhiều tùy chọn trong cùng một lệnh. Ví dụ:
  ```bash
  wc -l -w ten_tap.txt
  ```
- Sử dụng `cat` để xem nội dung tệp trước khi đếm:
  ```bash
  cat ten_tap.txt | wc -l
  ```
- Để đếm số dòng dài nhất trong tệp, bạn có thể sử dụng:
  ```bash
  wc -L ten_tap.txt
  ``` 

Lệnh `wc` là một công cụ đơn giản nhưng mạnh mẽ, giúp bạn nhanh chóng nắm bắt thông tin về nội dung của các tệp văn bản.