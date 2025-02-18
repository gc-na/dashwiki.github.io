# [台灣] Debian Almquist Shell (dash) trap 用法: 捕捉信號

## Overview
`trap` 命令用來捕捉和處理信號，這樣可以在腳本中對特定事件進行自定義的響應。當腳本接收到特定的信號時，可以執行指定的命令，這對於清理資源或處理異常情況非常有用。

## Usage
基本語法如下：
```sh
trap [options] [commands] [signals]
```

## Common Options
- `-p`: 顯示當前的 trap 設定。
- `-l`: 列出所有可用的信號名稱。

## Common Examples

### 1. 捕捉退出信號
當腳本接收到退出信號時，執行清理命令。
```sh
trap 'echo "清理中..."; rm -f /tmp/tempfile' EXIT
```

### 2. 捕捉中斷信號
當用戶按下 Ctrl+C 時，執行特定命令。
```sh
trap 'echo "中斷信號接收到，退出..." ; exit' INT
```

### 3. 捕捉終止信號
在接收到終止信號時，執行清理操作。
```sh
trap 'echo "終止信號接收到，正在清理..." ; exit' TERM
```

### 4. 顯示當前 trap 設定
使用 `-p` 選項來顯示當前的 trap 設定。
```sh
trap -p
```

## Tips
- 確保在腳本的開始部分設置 trap，以便能夠捕捉到信號。
- 使用 `trap` 來處理清理任務，這樣可以避免資源洩漏。
- 測試腳本時，注意信號的影響，確保 trap 行為符合預期。