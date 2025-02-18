# [台灣] Debian Almquist Shell (dash) true 使用方法: 總是返回成功

## Overview
`true` 命令是一個非常簡單的命令，它的主要功能是始終返回成功的退出狀態（0）。這在腳本中非常有用，特別是當你需要一個始終成功的命令來滿足某些條件時。

## Usage
基本語法如下：
```
true [options] [arguments]
```

## Common Options
`true` 命令並沒有特別的選項，因為它的功能非常簡單。它不接受任何參數或選項。

## Common Examples
以下是一些常見的使用範例：

1. **基本使用**
   ```sh
   true
   ```

2. **在條件語句中使用**
   ```sh
   if true; then
       echo "這是成功的條件"
   fi
   ```

3. **與其他命令結合使用**
   ```sh
   while true; do
       echo "這個循環會一直執行"
       sleep 1
   done
   ```

4. **用於測試命令**
   ```sh
   command_that_might_fail || true
   ```

## Tips
- `true` 可以用於腳本中，作為佔位符，讓你在未來可以替換成其他命令。
- 在需要一個始終返回成功的命令時，`true` 是一個簡單而有效的選擇。
- 結合 `&&` 或 `||` 使用時，可以控制命令的執行流程。