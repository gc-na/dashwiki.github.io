# [台灣] Debian Almquist Shell (dash) crontab 使用法: 設定定時任務

## Overview
`crontab` 命令用於管理用戶的定時任務。它允許用戶設定在特定時間自動執行的命令或腳本，這對於自動化日常任務非常有用。

## Usage
基本語法如下：
```bash
crontab [選項] [參數]
```

## Common Options
- `-e`：編輯當前用戶的 crontab 文件。
- `-l`：列出當前用戶的 crontab 任務。
- `-r`：刪除當前用戶的 crontab 文件。
- `-i`：在刪除 crontab 文件時顯示提示。

## Common Examples
- 編輯 crontab 文件：
  ```bash
  crontab -e
  ```

- 列出當前用戶的 crontab 任務：
  ```bash
  crontab -l
  ```

- 刪除當前用戶的 crontab 文件：
  ```bash
  crontab -r
  ```

- 設定每天凌晨 1 點執行一個備份腳本：
  ```bash
  0 1 * * * /path/to/backup.sh
  ```

- 每小時執行一次更新命令：
  ```bash
  0 * * * * apt update
  ```

## Tips
- 確保腳本具有執行權限，否則 crontab 將無法執行。
- 使用完整的路徑來指定命令或腳本，以避免路徑問題。
- 在 crontab 中添加註解，幫助未來的自己理解每個任務的目的。