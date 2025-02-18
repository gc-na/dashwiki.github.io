# [台灣] Debian Almquist Shell (dash) xargs 使用方法: 將輸入轉換為命令行參數

## Overview
`xargs` 是一個用於將標準輸入的數據轉換為命令行參數的工具。它通常與其他命令結合使用，以便處理大量的輸入數據，並將其傳遞給指定的命令。

## Usage
基本語法如下：
```bash
xargs [options] [arguments]
```

## Common Options
- `-n N`：每次傳遞 N 個參數給命令。
- `-d DELIM`：指定輸入的分隔符，預設為空格。
- `-p`：在執行每個命令之前提示用戶確認。
- `-0`：使用 null 字符作為輸入項的分隔符，通常與 `find` 命令的 `-print0` 選項一起使用。

## Common Examples
1. **將文件列表傳遞給 `rm` 命令**：
   ```bash
   find . -name "*.tmp" | xargs rm
   ```
   這個命令會找到當前目錄下所有以 `.tmp` 結尾的文件並刪除它們。

2. **限制每次傳遞的參數數量**：
   ```bash
   echo "one two three four five" | xargs -n 2 echo
   ```
   這會將輸出分成每次兩個參數，結果為：
   ```
   one two
   three four
   five
   ```

3. **使用自定義分隔符**：
   ```bash
   echo "apple;banana;cherry" | xargs -d ';' echo
   ```
   這會將分號作為分隔符，輸出為：
   ```
   apple banana cherry
   ```

4. **在執行前確認**：
   ```bash
   echo "file1.txt file2.txt" | xargs -p rm
   ```
   這會在刪除每個文件之前要求用戶確認。

## Tips
- 當處理包含空格的文件名時，使用 `-0` 選項搭配 `find` 的 `-print0` 來避免錯誤。
- 使用 `-n` 選項可以提高效率，特別是在處理大量文件時。
- 在使用 `xargs` 時，務必確認命令的安全性，特別是涉及刪除或修改文件的操作。