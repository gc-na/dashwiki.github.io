# [Hệ điều hành] Debian Almquist Shell (dash) gzip Cách sử dụng: Nén và giải nén tệp

## Tổng quan
Lệnh `gzip` được sử dụng để nén tệp tin, giúp giảm kích thước của chúng. Điều này rất hữu ích khi bạn cần tiết kiệm dung lượng lưu trữ hoặc khi bạn muốn truyền tải tệp qua mạng nhanh hơn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `gzip` như sau:

```bash
gzip [tùy chọn] [tệp tin]
```

## Các tùy chọn phổ biến
- `-d` hoặc `--decompress`: Giải nén tệp tin nén.
- `-k` hoặc `--keep`: Giữ lại tệp tin gốc sau khi nén.
- `-v` hoặc `--verbose`: Hiển thị thông tin chi tiết về quá trình nén.
- `-f` hoặc `--force`: Buộc nén tệp tin, ngay cả khi tệp tin đã tồn tại.

## Ví dụ phổ biến
- Nén một tệp tin:
```bash
gzip ten_tap_tin.txt
```

- Giải nén một tệp tin đã nén:
```bash
gzip -d ten_tap_tin.txt.gz
```

- Nén tệp tin và giữ lại tệp gốc:
```bash
gzip -k ten_tap_tin.txt
```

- Hiển thị thông tin chi tiết trong quá trình nén:
```bash
gzip -v ten_tap_tin.txt
```

## Mẹo
- Luôn kiểm tra dung lượng của tệp tin nén để đảm bảo rằng việc nén thực sự giúp tiết kiệm không gian.
- Sử dụng tùy chọn `-k` nếu bạn không muốn mất tệp tin gốc sau khi nén.
- Khi nén nhiều tệp tin, hãy cân nhắc sử dụng `tar` kết hợp với `gzip` để nén toàn bộ thư mục.