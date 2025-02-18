# [Hệ điều hành] Debian Almquist Shell (dash) umask: [quản lý quyền truy cập tệp]

## Tổng quan
Lệnh `umask` trong shell được sử dụng để thiết lập quyền truy cập mặc định cho các tệp và thư mục mới được tạo. Nó xác định các quyền nào sẽ bị từ chối khi tạo tệp hoặc thư mục, từ đó ảnh hưởng đến quyền truy cập của người dùng khác.

## Cú pháp
Cú pháp cơ bản của lệnh `umask` như sau:
```
umask [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `-S`: Hiển thị giá trị umask dưới dạng ký hiệu.
- `-p`: Hiển thị giá trị umask hiện tại của shell cha.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `umask`:

1. **Kiểm tra giá trị umask hiện tại:**
   ```sh
   umask
   ```

2. **Thiết lập umask mới:**
   ```sh
   umask 027
   ```

3. **Hiển thị umask dưới dạng ký hiệu:**
   ```sh
   umask -S
   ```

4. **Thiết lập umask cho phiên làm việc hiện tại:**
   ```sh
   umask 002
   ```

## Mẹo
- Hãy nhớ rằng giá trị umask được áp dụng cho các tệp và thư mục mới được tạo, vì vậy hãy thiết lập nó một cách hợp lý trước khi tạo các tệp quan trọng.
- Kiểm tra giá trị umask thường xuyên để đảm bảo rằng quyền truy cập của tệp được quản lý đúng cách.
- Sử dụng umask trong các script để đảm bảo rằng các tệp được tạo ra có quyền truy cập an toàn và phù hợp với yêu cầu bảo mật.