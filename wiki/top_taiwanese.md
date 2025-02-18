# [台灣] Debian Almquist Shell (dash) top 使用法: 監控系統資源

## Overview
`top` 命令是一個用於顯示系統中正在運行的進程和資源使用情況的工具。它提供了實時的系統性能監控，幫助用戶了解 CPU、記憶體和其他資源的使用狀況。

## Usage
基本語法如下：
```
top [options] [arguments]
```

## Common Options
- `-d <seconds>`: 設定更新間隔時間（以秒為單位）。
- `-n <number>`: 指定顯示的更新次數，之後自動退出。
- `-b`: 以批處理模式運行，適合將輸出重定向到文件。
- `-u <username>`: 只顯示指定用戶的進程。

## Common Examples
1. 以預設方式運行 `top`：
   ```bash
   top
   ```

2. 每 5 秒更新一次顯示：
   ```bash
   top -d 5
   ```

3. 顯示指定用戶的進程：
   ```bash
   top -u username
   ```

4. 以批處理模式運行並將輸出寫入文件：
   ```bash
   top -b -n 1 > top_output.txt
   ```

## Tips
- 使用 `Shift + M` 可以根據記憶體使用量排序進程。
- 按 `q` 鍵可以快速退出 `top`。
- 定期檢查 `top` 的輸出，幫助識別資源使用過高的進程，從而進行優化。