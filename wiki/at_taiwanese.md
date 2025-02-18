# [台灣] Debian Almquist Shell (dash) at 使用: 安排未來執行的任務

## Overview
`at` 命令用於安排在未來某個特定時間執行的任務。這使得用戶可以設定一次性任務，而不必持續運行一個進程來等待執行。

## Usage
基本語法如下：
```
at [options] [arguments]
```

## Common Options
- `-f FILE`：從指定的文件中讀取命令。
- `-m`：即使沒有輸出，也會發送郵件通知用戶。
- `-q QUEUE`：指定任務的隊列。
- `-l`：列出排定的任務。
- `-d JOB_ID`：刪除指定的任務。

## Common Examples
以下是一些常見的 `at` 命令範例：

1. 安排在明天下午 3 點執行 `backup.sh` 腳本：
   ```bash
   echo "/path/to/backup.sh" | at 15:00 tomorrow
   ```

2. 從文件中讀取命令並安排在指定時間執行：
   ```bash
   at -f /path/to/script.sh 09:00
   ```

3. 列出所有排定的任務：
   ```bash
   at -l
   ```

4. 刪除特定的任務（假設任務 ID 為 5）：
   ```bash
   at -d 5
   ```

## Tips
- 確保系統的 `atd` 服務正在運行，否則任務將無法執行。
- 使用 `-m` 選項來確保即使沒有輸出也能收到任務執行的通知。
- 可以使用 `atq` 命令來查看排定的任務，這是一個方便的替代方法。