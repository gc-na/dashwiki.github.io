# [Hệ điều hành] Debian Almquist Shell (dash) find cách sử dụng: Tìm kiếm tên tệp

## Tổng quan
Lệnh `find` trong shell Debian Almquist (dash) được sử dụng để tìm kiếm các tệp và thư mục trong hệ thống tệp dựa trên các tiêu chí nhất định như tên, kích thước, thời gian sửa đổi, và nhiều thuộc tính khác.

## Cách sử dụng
Cú pháp cơ bản của lệnh `find` như sau:
```
find [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-name <tên>`: Tìm các tệp có tên khớp với mẫu đã chỉ định.
- `-type <kiểu>`: Tìm các tệp theo loại (vd: `f` cho tệp thường, `d` cho thư mục).
- `-mtime <ngày>`: Tìm các tệp đã được sửa đổi trong một khoảng thời gian nhất định.
- `-size <kích thước>`: Tìm các tệp có kích thước cụ thể.
- `-exec <lệnh> {} \;`: Thực thi một lệnh trên các tệp được tìm thấy.

## Ví dụ phổ biến
- Tìm tất cả các tệp có đuôi `.txt` trong thư mục hiện tại:
  ```bash
  find . -name "*.txt"
  ```

- Tìm tất cả các thư mục trong thư mục `/home`:
  ```bash
  find /home -type d
  ```

- Tìm các tệp đã được sửa đổi trong 7 ngày qua:
  ```bash
  find . -mtime -7
  ```

- Tìm các tệp lớn hơn 1MB:
  ```bash
  find . -size +1M
  ```

- Thực thi lệnh `ls -l` trên tất cả các tệp `.log`:
  ```bash
  find . -name "*.log" -exec ls -l {} \;
  ```

## Mẹo
- Sử dụng `-iname` thay vì `-name` để tìm kiếm không phân biệt chữ hoa chữ thường.
- Kết hợp nhiều tùy chọn để tinh chỉnh kết quả tìm kiếm, ví dụ: `find . -type f -size +1M -mtime -30` để tìm các tệp lớn hơn 1MB và được sửa đổi trong 30 ngày qua.
- Luôn kiểm tra kết quả tìm kiếm trước khi thực hiện các lệnh với `-exec` để tránh thao tác trên các tệp không mong muốn.