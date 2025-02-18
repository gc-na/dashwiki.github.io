# [Hệ điều hành] Debian Almquist Shell (dash) mount: [gắn kết hệ thống tệp]

## Overview
Lệnh `mount` trong shell Debian Almquist (dash) được sử dụng để gắn kết một hệ thống tệp vào một điểm gắn kết trong hệ thống tệp hiện tại. Điều này cho phép người dùng truy cập vào các tệp và thư mục trên thiết bị lưu trữ khác nhau như ổ đĩa cứng, USB, hoặc các phân vùng khác.

## Usage
Cú pháp cơ bản của lệnh `mount` như sau:

```sh
mount [options] [arguments]
```

## Common Options
Dưới đây là một số tùy chọn phổ biến của lệnh `mount` cùng với giải thích ngắn gọn:

- `-t type`: Chỉ định loại hệ thống tệp (ví dụ: ext4, ntfs).
- `-o options`: Chỉ định các tùy chọn gắn kết (ví dụ: ro cho chỉ đọc, rw cho đọc và ghi).
- `-a`: Gắn kết tất cả các hệ thống tệp được liệt kê trong `/etc/fstab`.
- `-r`: Gắn kết hệ thống tệp ở chế độ chỉ đọc.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `mount`:

1. Gắn kết một phân vùng ext4 vào thư mục `/mnt/data`:

   ```sh
   mount -t ext4 /dev/sda1 /mnt/data
   ```

2. Gắn kết một ổ USB ở chế độ chỉ đọc:

   ```sh
   mount -o ro /dev/sdb1 /mnt/usb
   ```

3. Gắn kết tất cả các hệ thống tệp trong `/etc/fstab`:

   ```sh
   mount -a
   ```

4. Gắn kết một phân vùng NTFS với quyền đọc và ghi:

   ```sh
   mount -t ntfs-3g -o rw /dev/sdc1 /mnt/ntfs
   ```

## Tips
- Luôn kiểm tra xem điểm gắn kết đã tồn tại hay chưa trước khi gắn kết để tránh lỗi.
- Sử dụng lệnh `umount` để gỡ bỏ gắn kết hệ thống tệp khi không còn cần thiết.
- Kiểm tra quyền truy cập của người dùng để đảm bảo có thể gắn kết và truy cập vào hệ thống tệp.