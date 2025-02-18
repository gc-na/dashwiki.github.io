# [台灣] Debian Almquist Shell (dash) sed 使用方式: 文本處理工具

## Overview
`sed` 是一個流編輯器，用於對文本進行處理和轉換。它可以用來執行查找、替換、刪除等操作，特別適合於批量處理文本文件。

## Usage
基本語法如下：
```bash
sed [options] [arguments]
```

## Common Options
- `-e`: 允許多個編輯指令。
- `-f`: 從文件中讀取編輯指令。
- `-i`: 直接修改文件，而不是輸出到標準輸出。
- `-n`: 抑制自動輸出，只有使用 `p` 指令時才會輸出。

## Common Examples
以下是一些常見的 `sed` 使用範例：

1. **替換文本**
   將文件中的 "apple" 替換為 "orange"：
   ```bash
   sed 's/apple/orange/g' filename.txt
   ```

2. **刪除行**
   刪除文件中的第2行：
   ```bash
   sed '2d' filename.txt
   ```

3. **顯示特定行**
   顯示文件中的第3行：
   ```bash
   sed -n '3p' filename.txt
   ```

4. **從文件中讀取指令**
   從 `script.sed` 文件中讀取指令：
   ```bash
   sed -f script.sed filename.txt
   ```

5. **直接修改文件**
   直接在文件中替換 "foo" 為 "bar"：
   ```bash
   sed -i 's/foo/bar/g' filename.txt
   ```

## Tips
- 使用 `-n` 選項可以控制輸出，這在處理大型文件時非常有用。
- 在進行文件修改時，建議先備份原始文件，以防不小心刪除重要內容。
- 利用 `-e` 選項可以在同一條命令中執行多個操作，這樣可以提高效率。