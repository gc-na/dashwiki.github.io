# [Hệ điều hành Debian] Debian Almquist Shell (dash) basename: Lấy tên tệp từ đường dẫn

## Tổng quan
Lệnh `basename` được sử dụng để loại bỏ phần đường dẫn của một tệp, chỉ giữ lại tên tệp cuối cùng. Điều này hữu ích khi bạn muốn lấy tên tệp mà không cần thông tin về thư mục chứa nó.

## Cách sử dụng
Cú pháp cơ bản của lệnh `basename` như sau:
```
basename [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-a`: Xử lý nhiều tệp và trả về tên tệp cho từng tệp.
- `-s`: Loại bỏ phần mở rộng cụ thể khỏi tên tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `basename`:

1. Lấy tên tệp từ đường dẫn:
   ```sh
   basename /home/user/document.txt
   ```
   Kết quả: `document.txt`

2. Lấy tên tệp từ đường dẫn với phần mở rộng:
   ```sh
   basename /home/user/document.txt .txt
   ```
   Kết quả: `document`

3. Xử lý nhiều tệp:
   ```sh
   basename -a /home/user/file1.txt /home/user/file2.txt
   ```
   Kết quả:
   ```
   file1.txt
   file2.txt
   ```

4. Loại bỏ phần mở rộng cụ thể:
   ```sh
   basename /home/user/script.sh .sh
   ```
   Kết quả: `script`

## Mẹo
- Sử dụng `basename` trong các kịch bản shell để dễ dàng xử lý tên tệp mà không cần đường dẫn.
- Kết hợp `basename` với các lệnh khác như `find` để tự động lấy tên tệp từ kết quả tìm kiếm.
- Luôn kiểm tra xem tên tệp có phần mở rộng hay không trước khi sử dụng tùy chọn `-s` để tránh lỗi không mong muốn.