# [台灣] Debian Almquist Shell (dash) nohup 使用法: 允許程序在登出後繼續運行

## Overview
`nohup` 命令的主要功能是讓程序在使用者登出後仍然繼續運行。這對於需要長時間執行的任務特別有用，因為即使終端關閉，程序也不會受到影響。

## Usage
基本語法如下：
```
nohup [options] [arguments]
```

## Common Options
- `&`：將命令放在背景中運行。
- `-h`：顯示幫助信息。
- `-p`：指定要運行的程序的進程ID。

## Common Examples
以下是一些常見的使用範例：

1. 在背景中運行一個腳本：
   ```bash
   nohup ./myscript.sh &
   ```

2. 將輸出重定向到一個文件：
   ```bash
   nohup ./long_running_task > output.log &
   ```

3. 在不顯示任何輸出到終端的情況下運行：
   ```bash
   nohup ./silent_task > /dev/null 2>&1 &
   ```

4. 使用 nohup 執行一個 Python 腳本：
   ```bash
   nohup python3 myscript.py &
   ```

## Tips
- 確保在使用 `nohup` 時，將輸出重定向到文件，這樣可以方便後續查看程序的運行結果。
- 使用 `jobs` 命令可以查看當前背景運行的任務。
- 若要查看 `nohup` 生成的 `nohup.out` 文件，可以使用 `cat nohup.out` 命令。