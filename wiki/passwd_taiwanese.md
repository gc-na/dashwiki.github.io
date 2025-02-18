# [台灣] Debian Almquist Shell (dash) passwd 使用法: 更改使用者密碼

## Overview
`passwd` 命令用於更改使用者的密碼。這是一個重要的安全功能，確保只有授權的使用者能夠訪問系統。

## Usage
基本語法如下：
```
passwd [options] [username]
```

## Common Options
- `-d`：刪除使用者的密碼，允許無密碼登入。
- `-l`：鎖定使用者帳戶，禁止登入。
- `-u`：解鎖已鎖定的使用者帳戶。
- `-e`：強制使用者在下次登入時更改密碼。

## Common Examples
1. 更改當前使用者的密碼：
   ```bash
   passwd
   ```

2. 更改指定使用者的密碼（需要管理員權限）：
   ```bash
   sudo passwd username
   ```

3. 鎖定使用者帳戶：
   ```bash
   sudo passwd -l username
   ```

4. 解鎖使用者帳戶：
   ```bash
   sudo passwd -u username
   ```

5. 刪除使用者的密碼：
   ```bash
   sudo passwd -d username
   ```

6. 強制使用者在下次登入時更改密碼：
   ```bash
   sudo passwd -e username
   ```

## Tips
- 定期更改密碼以增強安全性。
- 使用強密碼，包含大小寫字母、數字及特殊符號。
- 在更改密碼後，記得確認是否能正常登入。