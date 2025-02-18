# [Hệ điều hành Debian] Debian Almquist Shell (dash) wget Cách sử dụng: Tải tệp từ Internet

## Tổng quan
Lệnh `wget` là một công cụ mạnh mẽ dùng để tải tệp từ Internet. Nó hỗ trợ nhiều giao thức như HTTP, HTTPS và FTP, cho phép người dùng tải xuống các tệp một cách dễ dàng và hiệu quả.

## Cách sử dụng
Cú pháp cơ bản của lệnh `wget` như sau:

```bash
wget [options] [arguments]
```

## Các tùy chọn phổ biến
- `-O <tên_tệp>`: Chỉ định tên tệp để lưu sau khi tải xuống.
- `-c`: Tiếp tục tải xuống một tệp bị gián đoạn.
- `-q`: Chạy trong chế độ im lặng, không hiển thị thông tin tải xuống.
- `--limit-rate=<tốc độ>`: Giới hạn tốc độ tải xuống.
- `-r`: Tải xuống các tệp theo cách đệ quy.

## Ví dụ thường gặp
- Tải xuống một tệp đơn giản:
  ```bash
  wget https://example.com/file.zip
  ```

- Tải xuống và lưu với tên khác:
  ```bash
  wget -O myfile.zip https://example.com/file.zip
  ```

- Tiếp tục tải xuống tệp bị gián đoạn:
  ```bash
  wget -c https://example.com/largefile.zip
  ```

- Tải xuống tệp trong chế độ im lặng:
  ```bash
  wget -q https://example.com/file.zip
  ```

- Tải xuống tất cả các tệp từ một trang web:
  ```bash
  wget -r https://example.com/
  ```

## Mẹo
- Sử dụng tùy chọn `-c` để tiết kiệm thời gian và băng thông khi tải xuống các tệp lớn.
- Kết hợp `--limit-rate` để tránh làm chậm kết nối Internet của bạn.
- Kiểm tra các tệp đã tải xuống bằng cách sử dụng tùy chọn `-q` để giảm thiểu thông tin hiển thị không cần thiết.