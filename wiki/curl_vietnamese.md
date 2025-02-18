# [Hệ điều hành] Debian Almquist Shell (dash) curl Cách sử dụng: Truy cập URL và tải dữ liệu

## Tổng quan
Lệnh `curl` được sử dụng để truyền tải dữ liệu đến hoặc từ một máy chủ thông qua các giao thức như HTTP, HTTPS, FTP, và nhiều giao thức khác. Đây là một công cụ mạnh mẽ cho việc kiểm tra và tương tác với các API hoặc tải xuống tệp từ Internet.

## Cách sử dụng
Cú pháp cơ bản của lệnh `curl` như sau:
```bash
curl [options] [arguments]
```

## Các tùy chọn phổ biến
- `-O`: Tải tệp và lưu với tên gốc.
- `-L`: Theo dõi các chuyển hướng.
- `-I`: Chỉ lấy tiêu đề HTTP.
- `-d`: Gửi dữ liệu trong yêu cầu POST.
- `-H`: Thêm tiêu đề tùy chỉnh vào yêu cầu.

## Ví dụ phổ biến
- Tải một tệp từ một URL:
  ```bash
  curl -O http://example.com/file.txt
  ```

- Theo dõi chuyển hướng và tải tệp:
  ```bash
  curl -L -O http://example.com/redirected-file.txt
  ```

- Lấy tiêu đề HTTP của một trang web:
  ```bash
  curl -I http://example.com
  ```

- Gửi dữ liệu POST đến một API:
  ```bash
  curl -d "param1=value1&param2=value2" http://example.com/api
  ```

- Thêm tiêu đề tùy chỉnh vào yêu cầu:
  ```bash
  curl -H "Authorization: Bearer token" http://example.com/protected-resource
  ```

## Mẹo
- Sử dụng `-v` để xem thông tin chi tiết về yêu cầu và phản hồi, hữu ích cho việc gỡ lỗi.
- Để lưu trữ đầu ra vào một tệp, bạn có thể sử dụng `-o filename.txt`.
- Kiểm tra các tùy chọn khác bằng cách sử dụng `curl --help` để tìm hiểu thêm về các tính năng của lệnh.