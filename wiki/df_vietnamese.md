# [Linux] Debian Almquist Shell (dash) df Cách sử dụng: Kiểm tra dung lượng đĩa

## Tổng quan
Lệnh `df` trong shell Debian Almquist (dash) được sử dụng để hiển thị thông tin về dung lượng đĩa còn trống và đã sử dụng trên các hệ thống tập tin. Nó giúp người dùng theo dõi tình trạng dung lượng của các phân vùng đĩa.

## Cách sử dụng
Cú pháp cơ bản của lệnh `df` như sau:

```bash
df [options] [arguments]
```

## Các tùy chọn phổ biến
- `-h`: Hiển thị dung lượng theo định dạng dễ đọc (KB, MB, GB).
- `-T`: Hiển thị loại hệ thống tập tin của mỗi phân vùng.
- `-a`: Bao gồm các hệ thống tập tin 0 byte.
- `-i`: Hiển thị thông tin về inode thay vì dung lượng.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `df`:

1. Hiển thị thông tin dung lượng đĩa cơ bản:
   ```bash
   df
   ```

2. Hiển thị dung lượng đĩa với định dạng dễ đọc:
   ```bash
   df -h
   ```

3. Hiển thị loại hệ thống tập tin:
   ```bash
   df -T
   ```

4. Hiển thị thông tin về inode:
   ```bash
   df -i
   ```

5. Bao gồm các hệ thống tập tin 0 byte:
   ```bash
   df -a
   ```

## Mẹo
- Sử dụng tùy chọn `-h` để dễ dàng đọc các giá trị dung lượng, đặc biệt khi làm việc với nhiều phân vùng.
- Kết hợp `df` với lệnh `grep` để tìm kiếm thông tin về một phân vùng cụ thể:
  ```bash
  df -h | grep /dev/sda1
  ```
- Thường xuyên kiểm tra dung lượng đĩa để tránh tình trạng đầy đĩa, có thể gây ra sự cố cho hệ thống.