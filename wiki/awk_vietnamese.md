# [Hệ điều hành Debian] Debian Almquist Shell (dash) awk Cách sử dụng: Truy xuất và xử lý văn bản

## Overview
`awk` là một ngôn ngữ lập trình mạnh mẽ được sử dụng để xử lý và phân tích văn bản, đặc biệt là các tệp văn bản có cấu trúc như CSV. Nó cho phép người dùng thực hiện các thao tác như lọc, định dạng và tính toán trên dữ liệu.

## Usage
Cú pháp cơ bản của lệnh `awk` như sau:

```bash
awk [options] [arguments]
```

## Common Options
- `-F`: Chỉ định ký tự phân cách (delimiter) cho các trường.
- `-v`: Đặt giá trị cho biến trước khi thực thi chương trình `awk`.
- `-f`: Chạy chương trình `awk` từ một tệp chứa mã lệnh.

## Common Examples
1. **In ra tất cả các dòng trong tệp:**
   ```bash
   awk '{print}' filename.txt
   ```

2. **Lọc các dòng có chứa từ khóa:**
   ```bash
   awk '/keyword/' filename.txt
   ```

3. **In ra trường thứ hai trong mỗi dòng:**
   ```bash
   awk '{print $2}' filename.txt
   ```

4. **Tính tổng của trường số trong cột đầu tiên:**
   ```bash
   awk '{sum += $1} END {print sum}' filename.txt
   ```

5. **Sử dụng ký tự phân cách khác (ví dụ, dấu phẩy):**
   ```bash
   awk -F, '{print $1}' filename.csv
   ```

## Tips
- Sử dụng `-F` để thay đổi ký tự phân cách khi làm việc với các tệp không phải là văn bản thuần túy.
- Thực hành với các tệp nhỏ trước khi áp dụng trên các tệp lớn để nắm vững cú pháp và cách hoạt động của `awk`.
- Kết hợp `awk` với các lệnh khác trong shell để tạo ra các quy trình tự động hóa mạnh mẽ.