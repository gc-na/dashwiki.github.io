# [Hệ điều hành] Debian Almquist Shell (dash) gunzip Cách sử dụng: Giải nén tệp tin gzip

## Tổng quan
Lệnh `gunzip` được sử dụng để giải nén các tệp tin nén có định dạng gzip. Nó giúp người dùng khôi phục lại các tệp tin về trạng thái ban đầu trước khi nén.

## Cách sử dụng
Cú pháp cơ bản của lệnh `gunzip` như sau:

```bash
gunzip [tùy chọn] [tệp tin]
```

## Tùy chọn phổ biến
- `-c`: Giải nén tệp và xuất ra stdout (màn hình) thay vì ghi đè lên tệp tin gốc.
- `-f`: Buộc giải nén, ghi đè lên các tệp tin đã tồn tại mà không hỏi.
- `-k`: Giữ lại tệp tin nén gốc sau khi giải nén.
- `-r`: Giải nén tất cả các tệp tin trong thư mục và các thư mục con.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `gunzip`:

1. Giải nén một tệp tin gzip:
   ```bash
   gunzip file.txt.gz
   ```

2. Giải nén và giữ lại tệp tin gốc:
   ```bash
   gunzip -k file.txt.gz
   ```

3. Giải nén tất cả các tệp tin gzip trong thư mục hiện tại:
   ```bash
   gunzip *.gz
   ```

4. Giải nén và xuất ra stdout:
   ```bash
   gunzip -c file.txt.gz > output.txt
   ```

## Mẹo
- Hãy luôn kiểm tra dung lượng ổ đĩa trước khi giải nén, vì tệp tin giải nén có thể chiếm nhiều không gian hơn.
- Sử dụng tùy chọn `-f` với cẩn thận, vì nó sẽ ghi đè lên các tệp tin mà không hỏi.
- Nếu bạn cần giải nén nhiều tệp tin, hãy sử dụng ký tự đại diện `*` để tiết kiệm thời gian.