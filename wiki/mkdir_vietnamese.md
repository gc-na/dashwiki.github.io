# [Hệ điều hành] Debian Almquist Shell (dash) mkdir Cách sử dụng: Tạo thư mục mới

## Tổng quan
Lệnh `mkdir` được sử dụng để tạo thư mục mới trong hệ thống tệp. Đây là một công cụ cơ bản nhưng rất hữu ích trong việc quản lý cấu trúc thư mục.

## Cách sử dụng
Cú pháp cơ bản của lệnh `mkdir` như sau:

```bash
mkdir [tùy chọn] [đối số]
```

## Tùy chọn phổ biến
- `-p`: Tạo các thư mục cha nếu chúng chưa tồn tại.
- `-v`: Hiển thị thông tin chi tiết về các thư mục được tạo.
- `-m`: Đặt quyền truy cập cho thư mục mới.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mkdir`:

1. Tạo một thư mục đơn giản:
    ```bash
    mkdir myfolder
    ```

2. Tạo nhiều thư mục cùng lúc:
    ```bash
    mkdir folder1 folder2 folder3
    ```

3. Tạo thư mục cha cùng với thư mục con:
    ```bash
    mkdir -p parent/child
    ```

4. Tạo thư mục và hiển thị thông tin:
    ```bash
    mkdir -v newfolder
    ```

5. Tạo thư mục với quyền truy cập cụ thể:
    ```bash
    mkdir -m 755 mysecurefolder
    ```

## Mẹo
- Sử dụng tùy chọn `-p` khi bạn không chắc chắn về sự tồn tại của các thư mục cha để tránh lỗi.
- Kiểm tra quyền truy cập của thư mục sau khi tạo để đảm bảo rằng nó phù hợp với nhu cầu của bạn.
- Đặt tên thư mục một cách rõ ràng và có tổ chức để dễ dàng quản lý sau này.