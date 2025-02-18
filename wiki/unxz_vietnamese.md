# [Hệ điều hành] Debian Almquist Shell (dash) unxz: Giải nén tệp .xz

## Overview
Lệnh `unxz` được sử dụng để giải nén các tệp có định dạng nén `.xz`. Đây là một công cụ hữu ích trong việc xử lý các tệp nén, giúp tiết kiệm không gian lưu trữ và giảm thời gian tải xuống.

## Usage
Cú pháp cơ bản của lệnh `unxz` như sau:
```
unxz [options] [arguments]
```

## Common Options
- `-k`, `--keep`: Giữ lại tệp gốc sau khi giải nén.
- `-f`, `--force`: Buộc ghi đè lên các tệp đã tồn tại mà không hỏi xác nhận.
- `-v`, `--verbose`: Hiển thị thông tin chi tiết trong quá trình giải nén.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `unxz`:

1. Giải nén một tệp `.xz`:
   ```bash
   unxz file.xz
   ```

2. Giải nén và giữ lại tệp gốc:
   ```bash
   unxz -k file.xz
   ```

3. Giải nén nhiều tệp cùng lúc:
   ```bash
   unxz file1.xz file2.xz file3.xz
   ```

4. Giải nén với thông tin chi tiết:
   ```bash
   unxz -v file.xz
   ```

5. Giải nén và ghi đè lên tệp đã tồn tại:
   ```bash
   unxz -f file.xz
   ```

## Tips
- Đảm bảo bạn có quyền ghi vào thư mục nơi tệp được giải nén.
- Sử dụng tùy chọn `-k` nếu bạn muốn giữ lại tệp nén gốc để sử dụng sau này.
- Kiểm tra kích thước tệp trước và sau khi giải nén để đảm bảo quá trình diễn ra thành công.