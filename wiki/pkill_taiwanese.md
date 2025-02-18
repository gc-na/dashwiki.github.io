# [台灣] Debian Almquist Shell (dash) pkill 使用法: 終止進程

## Overview
`pkill` 命令用於根據進程名稱或其他屬性終止進程。這是一個方便的工具，讓用戶可以快速終止不需要的程序，而不必查找進程ID（PID）。

## Usage
基本語法如下：
```
pkill [選項] [參數]
```

## Common Options
- `-f`：根據完整的命令行匹配進程名稱。
- `-n`：終止最新啟動的進程。
- `-o`：終止最早啟動的進程。
- `-signal`：指定要發送的信號，預設為 `TERM`。

## Common Examples
1. 根據進程名稱終止進程：
   ```bash
   pkill firefox
   ```

2. 根據完整命令行終止進程：
   ```bash
   pkill -f "python my_script.py"
   ```

3. 終止最新啟動的進程：
   ```bash
   pkill -n ssh
   ```

4. 終止最早啟動的進程：
   ```bash
   pkill -o nginx
   ```

5. 發送特定信號終止進程：
   ```bash
   pkill -9 apache2
   ```

## Tips
- 使用 `pkill -l` 可以列出所有可用的信號，幫助你選擇適合的信號來終止進程。
- 在使用 `pkill` 前，建議先使用 `pgrep` 命令確認要終止的進程名稱是否正確。
- 小心使用 `pkill`，因為它會終止所有匹配的進程，可能會影響系統的穩定性。