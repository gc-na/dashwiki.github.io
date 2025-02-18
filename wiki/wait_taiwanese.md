# [台灣] Debian Almquist Shell (dash) wait 用法: 等待子程序結束

## Overview
`wait` 命令用於等待一個或多個子程序的結束。在執行腳本時，這個命令可以確保在繼續執行後續命令之前，所有背景進程都已完成。

## Usage
基本語法如下：
```
wait [options] [arguments]
```

## Common Options
- `-n`：等待下一個子程序結束。
- `-p`：顯示子程序的退出狀態。

## Common Examples

### 等待所有背景進程
當你在腳本中啟動多個背景進程時，可以使用 `wait` 等待它們全部完成：
```sh
sleep 5 &
sleep 10 &
wait
echo "所有背景進程已完成"
```

### 等待特定的子程序
如果你知道某個特定的子程序的進程ID，可以使用該ID來等待：
```sh
sleep 5 &
PID=$!
wait $PID
echo "特定子程序已完成"
```

### 使用 -n 選項
使用 `-n` 選項可以等待下一個結束的子程序：
```sh
sleep 5 &
sleep 10 &
wait -n
echo "下一個子程序已完成"
```

## Tips
- 在腳本中使用 `wait` 可以避免因為背景進程未完成而導致的錯誤。
- 確保在使用 `wait` 前，已經啟動了背景進程，否則命令將立即返回。
- 使用 `wait` 可以幫助你獲取子程序的退出狀態，這對於錯誤處理非常有用。