# [Hệ điều hành] Debian Almquist Shell (dash) jobs: Quản lý tiến trình nền

## Overview
Lệnh `jobs` trong shell dash được sử dụng để hiển thị danh sách các tiến trình nền (background jobs) đang chạy trong phiên làm việc hiện tại. Nó giúp người dùng theo dõi và quản lý các tiến trình mà họ đã khởi động nhưng chưa kết thúc.

## Usage
Cú pháp cơ bản của lệnh `jobs` như sau:
```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Hiển thị PID (Process ID) của các tiến trình.
- `-n`: Chỉ hiển thị các tiến trình đã thay đổi trạng thái kể từ lần gọi lệnh trước đó.
- `-p`: Chỉ hiển thị PID của các tiến trình.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `jobs`:

1. **Hiển thị danh sách các tiến trình nền:**
   ```bash
   jobs
   ```

2. **Hiển thị danh sách các tiến trình nền với PID:**
   ```bash
   jobs -l
   ```

3. **Chỉ hiển thị các tiến trình đã thay đổi trạng thái:**
   ```bash
   jobs -n
   ```

4. **Hiển thị chỉ PID của các tiến trình:**
   ```bash
   jobs -p
   ```

## Tips
- Sử dụng lệnh `bg` để tiếp tục một tiến trình nền đã bị tạm dừng.
- Sử dụng lệnh `fg` để đưa một tiến trình nền về foreground.
- Kiểm tra trạng thái của tiến trình thường xuyên để quản lý hiệu quả hơn.