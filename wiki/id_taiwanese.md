# [台灣] Debian Almquist Shell (dash) id 使用法: 顯示使用者身份資訊

## Overview
`id` 命令用來顯示當前使用者的身份資訊，包括使用者 ID（UID）、群組 ID（GID）以及所屬的群組列表。

## Usage
基本語法如下：
```
id [options] [arguments]
```

## Common Options
- `-u`：顯示使用者的 UID。
- `-g`：顯示使用者的 GID。
- `-G`：顯示使用者所屬的所有群組 ID。
- `-n`：以名稱形式顯示 UID 和 GID，而不是數字。

## Common Examples
以下是一些常見的使用範例：

1. 顯示當前使用者的所有身份資訊：
   ```sh
   id
   ```

2. 顯示當前使用者的 UID：
   ```sh
   id -u
   ```

3. 顯示當前使用者的 GID：
   ```sh
   id -g
   ```

4. 顯示當前使用者所屬的所有群組 ID：
   ```sh
   id -G
   ```

5. 以名稱形式顯示當前使用者的 UID 和 GID：
   ```sh
   id -un
   ```

## Tips
- 使用 `id` 命令可以快速檢查使用者的權限和身份，特別是在進行系統管理時。
- 結合其他命令使用，例如 `grep`，可以過濾特定的群組資訊。
- 如果你需要檢查其他使用者的身份資訊，可以在命令後面加上使用者名稱，例如 `id username`。