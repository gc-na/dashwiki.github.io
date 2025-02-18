# [Hệ điều hành] Debian Almquist Shell (dash) mv Sử dụng: Di chuyển hoặc đổi tên tệp

## Overview
Lệnh `mv` trong shell Debian Almquist (dash) được sử dụng để di chuyển hoặc đổi tên các tệp và thư mục. Khi bạn muốn tổ chức lại các tệp của mình hoặc thay đổi tên chúng, lệnh này là công cụ hữu ích.

## Usage
Cú pháp cơ bản của lệnh `mv` như sau:

```bash
mv [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến cho lệnh `mv`:

- `-i`: Yêu cầu xác nhận trước khi ghi đè lên tệp đích nếu nó đã tồn tại.
- `-u`: Chỉ di chuyển tệp nếu tệp nguồn mới hơn tệp đích hoặc nếu tệp đích không tồn tại.
- `-v`: Hiển thị thông tin chi tiết về các tệp đang được di chuyển.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mv`:

1. **Di chuyển một tệp đến thư mục khác:**
   ```bash
   mv file.txt /path/to/destination/
   ```

2. **Đổi tên một tệp:**
   ```bash
   mv oldname.txt newname.txt
   ```

3. **Di chuyển nhiều tệp vào một thư mục:**
   ```bash
   mv file1.txt file2.txt /path/to/destination/
   ```

4. **Sử dụng tùy chọn xác nhận trước khi ghi đè:**
   ```bash
   mv -i file.txt /path/to/destination/
   ```

5. **Di chuyển tệp chỉ khi tệp nguồn mới hơn tệp đích:**
   ```bash
   mv -u file.txt /path/to/destination/
   ```

## Tips
- Luôn kiểm tra tệp đích trước khi di chuyển để tránh ghi đè lên tệp quan trọng.
- Sử dụng tùy chọn `-v` để theo dõi quá trình di chuyển, đặc biệt khi làm việc với nhiều tệp.
- Nếu bạn không chắc chắn về lệnh, hãy thử với tùy chọn `-i` để đảm bảo an toàn cho dữ liệu của bạn.