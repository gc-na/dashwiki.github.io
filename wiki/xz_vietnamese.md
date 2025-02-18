# [Hệ điều hành] Debian Almquist Shell (dash) xz: Nén và giải nén tệp tin

## Tổng quan
Lệnh `xz` được sử dụng để nén và giải nén các tệp tin bằng thuật toán nén LZMA. Nó giúp giảm kích thước tệp tin, tiết kiệm không gian lưu trữ và băng thông khi truyền tải.

## Cách sử dụng
Cú pháp cơ bản của lệnh `xz` như sau:
```
xz [options] [arguments]
```

## Các tùy chọn phổ biến
- `-d`, `--decompress`: Giải nén tệp tin.
- `-k`, `--keep`: Giữ lại tệp tin gốc sau khi nén.
- `-f`, `--force`: Buộc ghi đè lên tệp tin đã tồn tại.
- `-z`, `--compress`: Nén tệp tin (mặc định).
- `-9`: Sử dụng mức nén cao nhất.

## Ví dụ thường gặp
- Nén một tệp tin:
    ```bash
    xz file.txt
    ```
- Giải nén một tệp tin đã nén:
    ```bash
    xz -d file.txt.xz
    ```
- Nén tệp tin và giữ lại tệp gốc:
    ```bash
    xz -k file.txt
    ```
- Nén với mức nén cao nhất:
    ```bash
    xz -9 file.txt
    ```

## Mẹo
- Sử dụng tùy chọn `-k` nếu bạn muốn giữ lại tệp tin gốc trong khi nén.
- Kiểm tra kích thước tệp tin trước và sau khi nén để đánh giá hiệu quả của quá trình nén.
- Cân nhắc sử dụng mức nén `-9` cho các tệp tin lớn, nhưng lưu ý rằng quá trình nén sẽ mất nhiều thời gian hơn.