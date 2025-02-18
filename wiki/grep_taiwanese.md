# [台灣] Debian Almquist Shell (dash) grep 用法: 搜尋文本中的模式

## Overview
`grep` 是一個強大的命令行工具，用於在文本中搜尋特定的模式或字串。它可以從文件或標準輸入中過濾出符合條件的行，並將其顯示出來。

## Usage
基本語法如下：
```
grep [選項] [參數]
```

## Common Options
- `-i`：忽略大小寫。
- `-v`：反向匹配，顯示不符合模式的行。
- `-r`：遞迴搜尋子目錄中的文件。
- `-n`：顯示匹配行的行號。
- `-l`：僅顯示包含匹配模式的文件名。

## Common Examples
1. **基本搜尋**
   ```bash
   grep "hello" file.txt
   ```
   這將在 `file.txt` 中搜尋包含 "hello" 的行。

2. **忽略大小寫**
   ```bash
   grep -i "hello" file.txt
   ```
   這將在 `file.txt` 中搜尋 "hello" 或 "Hello" 等不同大小寫的匹配。

3. **反向匹配**
   ```bash
   grep -v "hello" file.txt
   ```
   這將顯示 `file.txt` 中不包含 "hello" 的所有行。

4. **遞迴搜尋**
   ```bash
   grep -r "hello" /path/to/directory
   ```
   這將在指定目錄及其子目錄中搜尋 "hello"。

5. **顯示行號**
   ```bash
   grep -n "hello" file.txt
   ```
   這將顯示 `file.txt` 中包含 "hello" 的行及其行號。

## Tips
- 使用 `-i` 選項可以讓搜尋更靈活，特別是在處理不確定大小寫的文本時。
- 結合 `-r` 和 `-l` 選項，可以快速找出哪些文件包含特定模式。
- 使用管道（`|`）將 `grep` 與其他命令結合，可以進行更複雜的文本處理。