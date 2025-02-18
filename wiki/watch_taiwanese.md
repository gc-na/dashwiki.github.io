# [台灣] Debian Almquist Shell (dash) watch 使用法: 監控命令輸出

## Overview
`watch` 命令用於定期執行指定的命令，並顯示其輸出。這對於監控系統狀態或變化非常有用，因為它可以自動更新顯示結果。

## Usage
基本語法如下：
```sh
watch [options] [arguments]
```

## Common Options
- `-n <seconds>`: 設定每次執行命令的間隔時間（以秒為單位）。
- `-d`: 高亮顯示輸出中的變化部分。
- `-t`: 隱藏標題，僅顯示命令的輸出。

## Common Examples
1. 每 2 秒查看當前系統的記憶體使用情況：
   ```sh
   watch -n 2 free -h
   ```

2. 監控當前目錄的檔案變化：
   ```sh
   watch -d ls -l
   ```

3. 每 5 秒檢查網路連接狀態：
   ```sh
   watch -n 5 ping -c 1 google.com
   ```

4. 隱藏標題，並每 10 秒查看 CPU 使用率：
   ```sh
   watch -t -n 10 top -b -n 1 | head -n 20
   ```

## Tips
- 使用 `-d` 選項可以幫助你快速識別變化，特別是在監控動態數據時。
- 設定適當的時間間隔，避免過於頻繁的執行，這可能會影響系統性能。
- 結合其他命令使用 `watch`，可以創建強大的監控工具，例如結合 `grep` 來過濾特定輸出。