# [Hệ điều hành] Debian Almquist Shell (dash) comm: So sánh hai tệp

## Overview
Lệnh `comm` được sử dụng để so sánh hai tệp đã được sắp xếp và hiển thị các dòng khác nhau và giống nhau giữa chúng. Lệnh này rất hữu ích trong việc phân tích sự khác biệt giữa hai danh sách hoặc tệp dữ liệu.

## Usage
Cú pháp cơ bản của lệnh `comm` như sau:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Ẩn các dòng chỉ có trong tệp đầu tiên.
- `-2`: Ẩn các dòng chỉ có trong tệp thứ hai.
- `-3`: Ẩn các dòng giống nhau trong cả hai tệp.
- `-i`: Bỏ qua sự khác biệt về chữ hoa chữ thường khi so sánh.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `comm`:

1. So sánh hai tệp và hiển thị tất cả các dòng:

```bash
comm file1.txt file2.txt
```

2. Hiển thị chỉ các dòng có trong `file1.txt` nhưng không có trong `file2.txt`:

```bash
comm -13 file1.txt file2.txt
```

3. Hiển thị chỉ các dòng có trong `file2.txt` nhưng không có trong `file1.txt`:

```bash
comm -12 file1.txt file2.txt
```

4. So sánh hai tệp mà không phân biệt chữ hoa chữ thường:

```bash
comm -i file1.txt file2.txt
```

## Tips
- Đảm bảo rằng các tệp được so sánh đã được sắp xếp trước khi sử dụng lệnh `comm`, nếu không, kết quả có thể không chính xác.
- Sử dụng các tùy chọn để tinh chỉnh đầu ra theo nhu cầu của bạn, giúp dễ dàng phân tích hơn.
- Nếu bạn cần so sánh nhiều hơn hai tệp, hãy xem xét sử dụng các công cụ khác như `diff` hoặc `sdiff`.