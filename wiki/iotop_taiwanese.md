# [台灣] Debian Almquist Shell (dash) iotop 使用法: 監控磁碟 I/O 活動

## Overview
iotop 是一個用於監控系統中磁碟 I/O 使用情況的工具。它可以顯示哪些進程正在進行磁碟讀取和寫入操作，並提供有關這些操作的詳細資訊。

## Usage
基本語法如下：
```
iotop [options] [arguments]
```

## Common Options
- `-o`：僅顯示有 I/O 活動的進程。
- `-b`：以批次模式運行，適合在腳本中使用。
- `-d <秒數>`：設定更新間隔時間，預設為 1 秒。
- `-p <PID>`：僅顯示指定進程 ID 的 I/O 活動。

## Common Examples
以下是一些常見的使用範例：

1. 以互動模式啟動 iotop：
   ```bash
   iotop
   ```

2. 僅顯示有 I/O 活動的進程：
   ```bash
   iotop -o
   ```

3. 以批次模式運行，並每 2 秒更新一次：
   ```bash
   iotop -b -d 2
   ```

4. 監控特定進程 ID 為 1234 的 I/O 活動：
   ```bash
   iotop -p 1234
   ```

## Tips
- 在使用 iotop 時，確保以 root 權限運行，以便獲取完整的 I/O 活動資訊。
- 如果系統中有大量進程，考慮使用 `-o` 選項來過濾顯示，這樣可以更容易找到有問題的進程。
- 定期檢查 I/O 活動可以幫助識別性能瓶頸，特別是在高負載的伺服器上。