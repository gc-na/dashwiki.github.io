# [台灣] Debian Almquist Shell (dash) dstat 使用法: 監控系統資源

## Overview
dstat 是一個強大的命令行工具，用於實時監控系統資源的使用情況。它可以同時顯示 CPU、記憶體、磁碟和網路等多種資源的統計資訊，幫助用戶了解系統的性能狀態。

## Usage
基本語法如下：
```bash
dstat [options] [arguments]
```

## Common Options
- `-c`：顯示 CPU 使用情況。
- `-d`：顯示磁碟 I/O 活動。
- `-n`：顯示網路流量。
- `-m`：顯示記憶體使用情況。
- `-t`：顯示時間戳。
- `--help`：顯示幫助資訊。

## Common Examples
以下是一些常見的 dstat 使用範例：

1. 顯示 CPU 和記憶體使用情況：
   ```bash
   dstat -c -m
   ```

2. 同時監控 CPU、磁碟和網路活動：
   ```bash
   dstat -c -d -n
   ```

3. 顯示帶有時間戳的所有資源使用情況：
   ```bash
   dstat -t -c -d -n -m
   ```

4. 以每秒更新一次的方式顯示系統資源：
   ```bash
   dstat 1
   ```

## Tips
- 使用 `dstat --help` 來查看所有可用的選項和參數。
- 可以將 dstat 的輸出重定向到檔案中，以便後續分析，例如：
  ```bash
  dstat -c -d -n > dstat_output.txt
  ```
- 結合其他命令使用，例如 `grep`，可以過濾特定的輸出資訊。