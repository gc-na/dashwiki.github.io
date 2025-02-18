# [Hệ điều hành] Debian Almquist Shell (dash) nslookup: [truy vấn thông tin DNS]

## Tổng quan
Lệnh `nslookup` được sử dụng để truy vấn thông tin từ hệ thống tên miền (DNS). Nó cho phép người dùng tìm kiếm địa chỉ IP của một tên miền hoặc ngược lại, tìm kiếm tên miền tương ứng với một địa chỉ IP.

## Cách sử dụng
Cú pháp cơ bản của lệnh `nslookup` như sau:

```
nslookup [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-type=TYPE`: Chỉ định loại bản ghi DNS cần truy vấn, ví dụ như A, AAAA, MX, TXT.
- `-timeout=TIME`: Đặt thời gian chờ cho một truy vấn DNS.
- `-retry=NUM`: Đặt số lần thử lại khi truy vấn không thành công.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `nslookup`:

1. **Tìm địa chỉ IP của một tên miền**:
   ```bash
   nslookup example.com
   ```

2. **Tìm tên miền tương ứng với một địa chỉ IP**:
   ```bash
   nslookup 93.184.216.34
   ```

3. **Truy vấn bản ghi MX của một tên miền**:
   ```bash
   nslookup -type=MX example.com
   ```

4. **Thay đổi máy chủ DNS để truy vấn**:
   ```bash
   nslookup example.com 8.8.8.8
   ```

## Mẹo
- Sử dụng tùy chọn `-type` để chỉ định loại bản ghi bạn muốn tìm kiếm, giúp tiết kiệm thời gian và tăng độ chính xác.
- Nếu bạn thường xuyên gặp lỗi khi truy vấn, hãy kiểm tra kết nối mạng hoặc thử sử dụng máy chủ DNS khác.
- Lưu ý rằng một số tên miền có thể không có bản ghi DNS công khai, vì vậy hãy chuẩn bị cho khả năng không tìm thấy kết quả.