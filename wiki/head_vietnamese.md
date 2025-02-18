# [Hệ điều hành Debian] Debian Almquist Shell (dash) head <Sử dụng tương đương>: Lấy dòng đầu tiên của tệp

## Tổng quan
Lệnh `head` trong shell cho phép bạn hiển thị một số dòng đầu tiên của một tệp. Đây là một công cụ hữu ích để xem nhanh nội dung của tệp mà không cần mở toàn bộ tệp đó.

## Cách sử dụng
Cú pháp cơ bản của lệnh `head` như sau:

```bash
head [options] [arguments]
```

## Các tùy chọn phổ biến
- `-n [số]`: Chỉ định số dòng bạn muốn hiển thị. Mặc định là 10 dòng.
- `-c [số]`: Hiển thị số byte đầu tiên của tệp.
- `-q`: Không hiển thị tiêu đề tệp khi có nhiều tệp được chỉ định.
- `-v`: Luôn hiển thị tiêu đề tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `head`:

1. Hiển thị 10 dòng đầu tiên của tệp `file.txt`:
   ```bash
   head file.txt
   ```

2. Hiển thị 5 dòng đầu tiên của tệp `file.txt`:
   ```bash
   head -n 5 file.txt
   ```

3. Hiển thị 20 byte đầu tiên của tệp `file.txt`:
   ```bash
   head -c 20 file.txt
   ```

4. Hiển thị 10 dòng đầu tiên của nhiều tệp:
   ```bash
   head file1.txt file2.txt
   ```

5. Hiển thị tiêu đề tệp ngay cả khi chỉ có một tệp:
   ```bash
   head -v file.txt
   ```

## Mẹo
- Sử dụng `head` kết hợp với `tail` để xem các phần đầu và cuối của tệp.
- Khi làm việc với các tệp lớn, `head` là một cách nhanh chóng để kiểm tra định dạng và nội dung mà không cần mở toàn bộ tệp.
- Bạn có thể sử dụng `head` trong các lệnh chuỗi để xử lý dữ liệu đầu vào từ các lệnh khác.