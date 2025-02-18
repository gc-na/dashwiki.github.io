# [Hệ điều hành] Debian Almquist Shell (dash) cmp Cách sử dụng: So sánh hai tệp tin

## Overview
Lệnh `cmp` trong shell Debian Almquist (dash) được sử dụng để so sánh hai tệp tin nhị phân. Nó xác định xem hai tệp có giống nhau hay không và nếu không, nó sẽ chỉ ra vị trí đầu tiên mà chúng khác nhau.

## Usage
Cú pháp cơ bản của lệnh `cmp` như sau:
```bash
cmp [options] [arguments]
```

## Common Options
- `-l`: Hiển thị các byte khác nhau và vị trí của chúng.
- `-s`: Không xuất ra thông tin, chỉ trả về mã thoát để cho biết tệp có giống nhau hay không.
- `-i OFFSET`: Bỏ qua OFFSET byte đầu tiên của tệp đầu vào.
- `-n N`: So sánh chỉ N byte đầu tiên của hai tệp.

## Common Examples
- So sánh hai tệp tin:
```bash
cmp file1.txt file2.txt
```

- So sánh hai tệp tin và chỉ hiển thị vị trí byte khác nhau:
```bash
cmp -l file1.bin file2.bin
```

- So sánh hai tệp tin mà không xuất ra thông tin, chỉ trả về mã thoát:
```bash
cmp -s file1.txt file2.txt
```

- So sánh chỉ 10 byte đầu tiên của hai tệp:
```bash
cmp -n 10 file1.bin file2.bin
```

## Tips
- Sử dụng tùy chọn `-s` để kiểm tra nhanh xem hai tệp có giống nhau hay không mà không cần xem chi tiết.
- Khi làm việc với tệp nhị phân, hãy sử dụng tùy chọn `-l` để có cái nhìn rõ hơn về sự khác biệt giữa các tệp.
- Nếu bạn chỉ quan tâm đến một phần cụ thể của tệp, hãy sử dụng tùy chọn `-n` để giới hạn số byte được so sánh.