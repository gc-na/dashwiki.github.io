# [Hệ điều hành] Debian Almquist Shell (dash) umount: [ngắt kết nối hệ thống tệp]

## Tổng quan
Lệnh `umount` được sử dụng để ngắt kết nối một hệ thống tệp đã được gắn kết. Khi bạn không còn cần truy cập vào một hệ thống tệp nào đó, việc sử dụng `umount` giúp giải phóng tài nguyên và đảm bảo rằng dữ liệu được lưu trữ an toàn.

## Cách sử dụng
Cú pháp cơ bản của lệnh `umount` như sau:
```
umount [tùy chọn] [tham số]
```

## Tùy chọn phổ biến
- `-a`: Ngắt kết nối tất cả các hệ thống tệp được gắn kết trong tệp `/etc/mtab`.
- `-f`: Ngắt kết nối một hệ thống tệp ngay cả khi nó đang được sử dụng.
- `-l`: Ngắt kết nối một hệ thống tệp một cách "lười biếng", tức là sẽ thực hiện ngắt kết nối khi không còn truy cập vào hệ thống tệp đó.
- `-r`: Ngắt kết nối và gắn lại hệ thống tệp ở chế độ đọc.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `umount`:

1. Ngắt kết nối một hệ thống tệp cụ thể:
   ```bash
   umount /mnt/usb
   ```

2. Ngắt kết nối tất cả các hệ thống tệp:
   ```bash
   umount -a
   ```

3. Ngắt kết nối một hệ thống tệp ngay cả khi đang được sử dụng:
   ```bash
   umount -f /mnt/network
   ```

4. Ngắt kết nối một hệ thống tệp một cách "lười biếng":
   ```bash
   umount -l /mnt/temporary
   ```

## Mẹo
- Trước khi ngắt kết nối, hãy đảm bảo rằng không có tiến trình nào đang sử dụng hệ thống tệp đó để tránh mất dữ liệu.
- Sử dụng lệnh `df` để kiểm tra các hệ thống tệp đang được gắn kết trước khi thực hiện ngắt kết nối.
- Nếu gặp lỗi khi ngắt kết nối, hãy kiểm tra xem có tệp nào đang mở trong hệ thống tệp đó hay không.