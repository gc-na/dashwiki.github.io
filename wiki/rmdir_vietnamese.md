# [Hệ điều hành] Debian Almquist Shell (dash) rmdir: Xóa thư mục rỗng

## Tổng quan
Lệnh `rmdir` được sử dụng để xóa các thư mục rỗng trong hệ thống tệp. Nếu thư mục không rỗng, lệnh sẽ không thực hiện xóa và sẽ thông báo lỗi.

## Cú pháp
Cú pháp cơ bản của lệnh `rmdir` như sau:
```
rmdir [tùy chọn] [đối số]
```

## Tùy chọn thông dụng
- `--ignore-fail-on-non-empty`: Bỏ qua lỗi nếu thư mục không rỗng.
- `--verbose`: Hiển thị thông tin chi tiết về các thư mục đã được xóa.

## Ví dụ thông dụng
Dưới đây là một số ví dụ về cách sử dụng lệnh `rmdir`:

1. Xóa một thư mục rỗng:
   ```bash
   rmdir thu_muc_rong
   ```

2. Xóa nhiều thư mục rỗng cùng một lúc:
   ```bash
   rmdir thu_muc1 thu_muc2 thu_muc3
   ```

3. Sử dụng tùy chọn `--verbose` để xem thông tin chi tiết:
   ```bash
   rmdir --verbose thu_muc_rong
   ```

4. Bỏ qua lỗi nếu thư mục không rỗng:
   ```bash
   rmdir --ignore-fail-on-non-empty thu_muc_khong_rong
   ```

## Mẹo
- Trước khi sử dụng `rmdir`, hãy chắc chắn rằng thư mục bạn muốn xóa là rỗng để tránh thông báo lỗi.
- Sử dụng tùy chọn `--verbose` để theo dõi các thư mục đã được xóa, điều này hữu ích khi bạn xóa nhiều thư mục cùng một lúc.
- Nếu bạn cần xóa thư mục không rỗng, hãy sử dụng lệnh `rm -r` thay vì `rmdir`.