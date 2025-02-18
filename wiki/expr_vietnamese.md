# [Hệ điều hành] Debian Almquist Shell (dash) expr Cách sử dụng: [thực hiện các phép toán và so sánh]

## Overview
Lệnh `expr` trong shell dash được sử dụng để thực hiện các phép toán số học, so sánh và xử lý chuỗi. Nó cho phép người dùng tính toán và kiểm tra các điều kiện trong các kịch bản shell.

## Usage
Cú pháp cơ bản của lệnh `expr` như sau:

```bash
expr [options] [arguments]
```

## Common Options
- `-e`: Cho phép sử dụng biểu thức phức tạp.
- `-s`: Bỏ qua các khoảng trắng trong đầu vào.
- `length`: Tính độ dài của một chuỗi.

## Common Examples

### 1. Thực hiện phép cộng
```bash
expr 5 + 3
```
Kết quả: `8`

### 2. Thực hiện phép trừ
```bash
expr 10 - 4
```
Kết quả: `6`

### 3. So sánh hai số
```bash
expr 5 \> 3
```
Kết quả: `1` (đúng)

### 4. Tính độ dài của một chuỗi
```bash
expr length "Hello World"
```
Kết quả: `11`

### 5. Kết hợp các phép toán
```bash
expr \( 5 + 3 \) \* 2
```
Kết quả: `16`

## Tips
- Sử dụng dấu `\` trước các ký tự đặc biệt như `(`, `)`, `>`, `<` để tránh nhầm lẫn với các ký tự trong shell.
- Đảm bảo rằng các toán hạng trong phép toán được phân cách bằng khoảng trắng để `expr` có thể nhận diện đúng.
- Khi làm việc với chuỗi, hãy nhớ rằng `expr` không hỗ trợ các phép toán chuỗi phức tạp, vì vậy hãy sử dụng các công cụ khác nếu cần.