# [Hệ điều hành] Debian Almquist Shell (dash) bg: [chạy tiến trình nền]

## Tổng quan
Lệnh `bg` trong shell Debian Almquist (dash) được sử dụng để tiếp tục một tiến trình đã bị tạm dừng và chạy nó ở chế độ nền. Điều này cho phép người dùng tiếp tục sử dụng shell trong khi tiến trình vẫn hoạt động.

## Cách sử dụng
Cú pháp cơ bản của lệnh `bg` như sau:
```
bg [options] [arguments]
```

## Tùy chọn phổ biến
- Không có tùy chọn cụ thể nào cho lệnh `bg`, nhưng bạn có thể chỉ định số của tiến trình (job number) để xác định tiến trình nào sẽ được đưa vào nền.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `bg`:

1. **Tiếp tục một tiến trình đã tạm dừng**:
   Giả sử bạn đã tạm dừng một tiến trình bằng cách nhấn `Ctrl+Z`, bạn có thể tiếp tục nó ở chế độ nền bằng lệnh:
   ```bash
   bg
   ```

2. **Tiếp tục một tiến trình cụ thể**:
   Nếu bạn có nhiều tiến trình đang chạy và muốn tiếp tục một tiến trình cụ thể, bạn có thể chỉ định số của tiến trình:
   ```bash
   bg %1
   ```
   (Ở đây, `%1` là số của tiến trình bạn muốn tiếp tục.)

3. **Kiểm tra tiến trình nền**:
   Sau khi đưa một tiến trình vào nền, bạn có thể kiểm tra các tiến trình đang chạy bằng lệnh:
   ```bash
   jobs
   ```

## Mẹo
- Hãy chắc chắn rằng bạn đã tạm dừng tiến trình bằng `Ctrl+Z` trước khi sử dụng lệnh `bg`.
- Sử dụng lệnh `jobs` để theo dõi các tiến trình đang chạy và đã tạm dừng, giúp bạn dễ dàng quản lý chúng.
- Nếu bạn muốn đưa một tiến trình trở lại chế độ nền và không cần tương tác với nó, hãy sử dụng `bg` để không làm gián đoạn công việc của bạn trên shell.