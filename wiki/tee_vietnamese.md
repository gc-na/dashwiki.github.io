# [Hệ điều hành] Debian Almquist Shell (dash) tee <Sử dụng tương đương>: Ghi dữ liệu vào tệp và xuất ra đầu ra chuẩn

## Tổng quan
Lệnh `tee` trong shell cho phép bạn ghi dữ liệu vào một hoặc nhiều tệp đồng thời với việc xuất dữ liệu đó ra đầu ra chuẩn. Điều này rất hữu ích khi bạn muốn theo dõi đầu ra của một lệnh trong khi cũng lưu trữ nó.

## Cách sử dụng
Cú pháp cơ bản của lệnh `tee` như sau:
```bash
tee [tùy chọn] [tham số]
```

## Các tùy chọn phổ biến
- `-a`: Ghi dữ liệu vào cuối tệp thay vì ghi đè lên tệp.
- `-i`: Bỏ qua tín hiệu ngắt (interrupt) từ người dùng.
- `-p`: In ra thông báo lỗi nếu không thể ghi vào tệp.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `tee`:

1. Ghi đầu ra của lệnh `ls` vào tệp `output.txt`:
   ```bash
   ls | tee output.txt
   ```

2. Ghi đầu ra của lệnh `echo` vào tệp và đồng thời hiển thị trên màn hình:
   ```bash
   echo "Hello, World!" | tee hello.txt
   ```

3. Ghi đầu ra của lệnh `cat` vào tệp `data.txt` và thêm vào cuối tệp:
   ```bash
   cat file.txt | tee -a data.txt
   ```

4. Ghi đầu ra của lệnh `grep` vào tệp `results.txt` và hiển thị trên màn hình:
   ```bash
   grep "pattern" input.txt | tee results.txt
   ```

## Mẹo
- Sử dụng tùy chọn `-a` khi bạn muốn thêm dữ liệu vào tệp mà không ghi đè lên nội dung hiện có.
- Kết hợp `tee` với các lệnh khác trong pipeline để dễ dàng theo dõi và lưu trữ đầu ra.
- Đảm bảo rằng bạn có quyền ghi vào tệp mà bạn đang cố gắng ghi dữ liệu; nếu không, lệnh sẽ không thực hiện thành công.