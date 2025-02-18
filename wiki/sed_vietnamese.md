# [Hệ điều hành] Debian Almquist Shell (dash) sed Cách sử dụng: Thay thế văn bản trong tệp

## Tổng quan
Lệnh `sed` (stream editor) là một công cụ mạnh mẽ trong hệ thống Unix/Linux dùng để xử lý và chỉnh sửa văn bản trong dòng. Nó cho phép người dùng thực hiện các thao tác như thay thế, xóa hoặc chèn văn bản trong các tệp hoặc đầu vào từ dòng lệnh.

## Cách sử dụng
Cú pháp cơ bản của lệnh `sed` như sau:

```bash
sed [options] [arguments]
```

## Các tùy chọn phổ biến
- `-e`: Chỉ định một lệnh `sed` để thực hiện.
- `-i`: Thay đổi trực tiếp tệp đầu vào (in-place).
- `-n`: Ngăn chặn việc in ra tất cả các dòng, chỉ in ra các dòng được chỉ định.
- `s/pattern/replacement/`: Thay thế `pattern` bằng `replacement`.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `sed`:

1. **Thay thế một từ trong tệp:**
   ```bash
   sed 's/oldword/newword/' filename.txt
   ```

2. **Thay thế tất cả các từ trong tệp:**
   ```bash
   sed 's/oldword/newword/g' filename.txt
   ```

3. **Thay đổi trực tiếp tệp:**
   ```bash
   sed -i 's/oldword/newword/g' filename.txt
   ```

4. **In ra các dòng chứa một từ cụ thể:**
   ```bash
   sed -n '/pattern/p' filename.txt
   ```

5. **Xóa các dòng chứa một từ cụ thể:**
   ```bash
   sed '/pattern/d' filename.txt
   ```

## Mẹo
- Sử dụng tùy chọn `-i` với cẩn thận, vì nó sẽ thay đổi tệp gốc. Bạn có thể tạo một bản sao lưu bằng cách sử dụng `-i.bak`.
- Kiểm tra kết quả trước khi thay đổi bằng cách không sử dụng tùy chọn `-i`.
- Kết hợp `sed` với các lệnh khác như `grep` hoặc `awk` để xử lý văn bản phức tạp hơn.