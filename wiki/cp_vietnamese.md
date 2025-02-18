# [Hệ điều hành] Debian Almquist Shell (dash) cp Cách sử dụng: Sao chép tệp và thư mục

## Tổng quan
Lệnh `cp` trong shell dùng để sao chép tệp và thư mục từ vị trí này sang vị trí khác. Đây là một công cụ cơ bản nhưng rất hữu ích trong việc quản lý tệp trên hệ thống.

## Cách sử dụng
Cú pháp cơ bản của lệnh `cp` như sau:
```
cp [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-r`: Sao chép thư mục và tất cả nội dung bên trong.
- `-i`: Yêu cầu xác nhận trước khi ghi đè lên tệp đã tồn tại.
- `-u`: Chỉ sao chép tệp nếu tệp nguồn mới hơn tệp đích hoặc nếu tệp đích không tồn tại.
- `-v`: Hiển thị thông tin chi tiết về quá trình sao chép.

## Ví dụ phổ biến
- Sao chép một tệp:
  ```bash
  cp file1.txt file2.txt
  ```
- Sao chép một thư mục cùng với tất cả nội dung:
  ```bash
  cp -r folder1/ folder2/
  ```
- Sao chép tệp và yêu cầu xác nhận nếu tệp đích đã tồn tại:
  ```bash
  cp -i file1.txt file2.txt
  ```
- Sao chép tệp chỉ khi tệp nguồn mới hơn tệp đích:
  ```bash
  cp -u file1.txt file2.txt
  ```

## Mẹo
- Luôn sử dụng tùy chọn `-i` khi sao chép tệp để tránh ghi đè lên tệp quan trọng.
- Kiểm tra lại đường dẫn tệp trước khi thực hiện lệnh để đảm bảo bạn đang sao chép đến đúng vị trí.
- Sử dụng tùy chọn `-v` để theo dõi quá trình sao chép, đặc biệt khi làm việc với nhiều tệp hoặc thư mục lớn.