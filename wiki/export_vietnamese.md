# [Hệ điều hành] Debian Almquist Shell (dash) export <Sử dụng tương đương>: Thiết lập biến môi trường

## Tổng quan
Lệnh `export` trong shell dash được sử dụng để thiết lập và xuất các biến môi trường, cho phép các biến này có thể được truy cập bởi các tiến trình con. Khi một biến được xuất, nó trở thành một phần của môi trường của shell và có thể được sử dụng bởi các chương trình hoặc script khác.

## Cú pháp
Cú pháp cơ bản của lệnh `export` như sau:
```sh
export [tùy chọn] [biến=giá trị]
```

## Các tùy chọn phổ biến
- `-n`: Ngừng xuất một biến đã được xuất trước đó.
- `-p`: Hiển thị tất cả các biến môi trường đã được xuất.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `export`:

1. Xuất một biến môi trường:
   ```sh
   export MY_VAR="Hello World"
   ```

2. Kiểm tra biến đã được xuất:
   ```sh
   echo $MY_VAR
   ```

3. Xuất nhiều biến cùng một lúc:
   ```sh
   export VAR1="Value1" VAR2="Value2"
   ```

4. Ngừng xuất một biến:
   ```sh
   export -n MY_VAR
   ```

5. Hiển thị tất cả các biến môi trường đã được xuất:
   ```sh
   export -p
   ```

## Mẹo
- Hãy chắc chắn rằng bạn xuất biến môi trường trước khi chạy các script hoặc chương trình cần đến biến đó.
- Sử dụng lệnh `export` trong file cấu hình shell như `.bashrc` hoặc `.profile` để tự động thiết lập các biến môi trường khi bạn đăng nhập.
- Để tránh xung đột, hãy sử dụng tên biến rõ ràng và có ý nghĩa.