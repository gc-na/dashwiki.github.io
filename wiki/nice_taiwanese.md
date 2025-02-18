# [台灣] Debian Almquist Shell (dash) nice 使用法: 調整程序優先權

## Overview
`nice` 命令用於調整執行程序的優先權。透過這個命令，使用者可以指定一個程序在系統資源分配中的優先級，讓系統能夠更有效地管理多個同時運行的程序。

## Usage
基本語法如下：
```
nice [options] [arguments]
```

## Common Options
- `-n, --adjustment=N`：指定優先權的調整值，範圍從 -20（最高優先權）到 19（最低優先權）。
- `--help`：顯示幫助信息。
- `--version`：顯示版本信息。

## Common Examples
1. **以默認優先權執行程序**
   ```bash
   nice my_program
   ```

2. **以較低優先權執行程序**
   ```bash
   nice -n 10 my_program
   ```

3. **以較高優先權執行程序**
   ```bash
   nice -n -5 my_program
   ```

4. **查看當前優先權**
   ```bash
   ps -o pid,ni,comm
   ```

## Tips
- 使用 `nice` 時，請注意調整的值會影響程序的執行效率，選擇合適的優先權非常重要。
- 在執行需要大量資源的程序時，可以考慮使用較低的優先權，以避免影響其他重要程序的運行。
- 如果需要更改已在運行的程序的優先權，可以使用 `renice` 命令。