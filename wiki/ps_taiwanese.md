# [台灣] Debian Almquist Shell (dash) ps 使用法: 顯示當前進程資訊

## Overview
`ps` 命令用於顯示當前系統中運行的進程資訊。它可以幫助用戶查看進程的狀態、使用的資源以及其他相關資訊。

## Usage
基本語法如下：
```
ps [options] [arguments]
```

## Common Options
- `-e`：顯示所有進程。
- `-f`：以完整格式顯示進程資訊。
- `-u [user]`：顯示指定用戶的進程。
- `-p [pid]`：顯示特定進程ID的進程。
- `aux`：顯示所有用戶的進程，包括詳細資訊。

## Common Examples
- 顯示所有進程：
  ```bash
  ps -e
  ```

- 以完整格式顯示進程：
  ```bash
  ps -ef
  ```

- 顯示特定用戶的進程：
  ```bash
  ps -u username
  ```

- 顯示特定進程ID的進程：
  ```bash
  ps -p 1234
  ```

- 顯示所有進程及詳細資訊：
  ```bash
  ps aux
  ```

## Tips
- 使用 `ps aux` 可以獲得最詳細的進程資訊，適合進行系統監控。
- 結合 `grep` 命令可以輕鬆查找特定進程，例如：
  ```bash
  ps aux | grep process_name
  ```
- 定期檢查進程狀態，有助於維持系統的穩定性。