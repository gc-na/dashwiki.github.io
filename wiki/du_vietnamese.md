# [Hệ điều hành] Debian Almquist Shell (dash) du: [tính toán kích thước thư mục]

## Tổng quan
Lệnh `du` (disk usage) được sử dụng để ước lượng kích thước của các tệp và thư mục trên hệ thống. Nó giúp người dùng biết được dung lượng mà các tệp và thư mục đang chiếm dụng trên đĩa cứng.

## Cú pháp
Cú pháp cơ bản của lệnh `du` như sau:
```
du [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-h`: Hiển thị kích thước theo định dạng dễ đọc (KB, MB, GB).
- `-s`: Tóm tắt kích thước tổng cộng của thư mục mà không liệt kê từng tệp.
- `-a`: Hiển thị kích thước của tất cả các tệp, không chỉ thư mục.
- `-c`: Tính tổng kích thước của tất cả các thư mục và tệp được liệt kê.

## Ví dụ thường gặp
- Để xem kích thước của thư mục hiện tại:
  ```bash
  du
  ```

- Để xem kích thước của thư mục hiện tại với định dạng dễ đọc:
  ```bash
  du -h
  ```

- Để tóm tắt kích thước tổng cộng của thư mục:
  ```bash
  du -sh
  ```

- Để liệt kê kích thước của tất cả các tệp trong thư mục hiện tại:
  ```bash
  du -a
  ```

- Để tính tổng kích thước của tất cả các thư mục và tệp trong một thư mục cụ thể:
  ```bash
  du -ch /path/to/directory
  ```

## Mẹo
- Sử dụng tùy chọn `-h` để dễ dàng đọc kích thước, đặc biệt khi làm việc với các thư mục lớn.
- Kết hợp `du` với lệnh `sort` để sắp xếp các thư mục theo kích thước:
  ```bash
  du -h | sort -h
  ```
- Nếu bạn chỉ quan tâm đến một thư mục cụ thể, hãy chỉ định đường dẫn của nó để tiết kiệm thời gian tính toán.