# [Hệ điều hành] Debian Almquist Shell (dash) groups: Nhóm người dùng

## Overview
Lệnh `groups` trong dash được sử dụng để hiển thị các nhóm mà một người dùng thuộc về. Nó giúp người dùng biết được quyền hạn và vai trò của họ trong hệ thống thông qua các nhóm mà họ đã tham gia.

## Usage
Cú pháp cơ bản của lệnh `groups` như sau:

```bash
groups [options] [arguments]
```

## Common Options
- `-h`, `--help`: Hiển thị thông tin trợ giúp về lệnh `groups`.
- `-n`, `--no-name`: Chỉ hiển thị ID nhóm thay vì tên nhóm.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `groups`:

1. **Hiển thị các nhóm của người dùng hiện tại:**
   ```bash
   groups
   ```

2. **Hiển thị các nhóm của một người dùng cụ thể:**
   ```bash
   groups username
   ```

3. **Hiển thị ID nhóm thay vì tên nhóm:**
   ```bash
   groups -n username
   ```

4. **Hiển thị thông tin trợ giúp:**
   ```bash
   groups --help
   ```

## Tips
- Sử dụng lệnh `groups` để kiểm tra quyền truy cập của bạn trong hệ thống, đặc biệt khi bạn cần xác định quyền hạn cho các tác vụ cụ thể.
- Nếu bạn là quản trị viên, hãy sử dụng lệnh này để xác định các nhóm mà người dùng thuộc về để quản lý quyền truy cập hiệu quả hơn.