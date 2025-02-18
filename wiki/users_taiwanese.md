# [台灣] Debian Almquist Shell (dash) 使用者命令: 查詢使用者資訊

## Overview
`users` 命令用於顯示當前登入系統的使用者名稱。這是一個簡單而有效的工具，能夠快速獲取系統上活躍使用者的資訊。

## Usage
基本語法如下：
```
users [options] [arguments]
```

## Common Options
- `-n`：只顯示使用者名稱，不顯示其他資訊。

## Common Examples
以下是一些常見的使用範例：

1. **顯示當前登入的所有使用者**：
   ```sh
   users
   ```

2. **顯示當前登入的使用者名稱（使用 -n 選項）**：
   ```sh
   users -n
   ```

3. **在腳本中使用 users 命令**：
   ```sh
   current_users=$(users)
   echo "當前登入的使用者有: $current_users"
   ```

## Tips
- `users` 命令的輸出不會顯示重複的使用者名稱，因此如果多個會話由同一使用者登入，該使用者只會顯示一次。
- 此命令非常適合用於監控和管理系統，特別是在多使用者環境中。