# [台灣] Debian Almquist Shell (dash) wc 使用方法: 計算文件的行數、字數和字元數

## Overview
`wc` 命令是用來計算文件中的行數、字數和字元數的工具。它可以幫助使用者快速獲取文本文件的統計信息，對於分析和處理文本數據非常有用。

## Usage
基本語法如下：
```bash
wc [選項] [參數]
```

## Common Options
- `-l`：計算行數。
- `-w`：計算字數。
- `-c`：計算字元數。
- `-m`：計算字符數（包括多字節字符）。
- `-L`：顯示文件中最長行的長度。

## Common Examples
以下是一些常見的使用範例：

1. 計算文件的行數：
   ```bash
   wc -l filename.txt
   ```

2. 計算文件的字數：
   ```bash
   wc -w filename.txt
   ```

3. 計算文件的字元數：
   ```bash
   wc -c filename.txt
   ```

4. 同時計算行數、字數和字元數：
   ```bash
   wc filename.txt
   ```

5. 計算多個文件的行數：
   ```bash
   wc -l file1.txt file2.txt
   ```

## Tips
- 使用 `wc` 與其他命令結合，例如使用管道（`|`）來計算命令輸出的行數：
  ```bash
  ls -l | wc -l
  ```
- 當處理多個文件時，`wc` 會在每個文件的統計後顯示文件名，這樣可以輕鬆辨識結果。
- 可以使用 `-m` 選項來確保計算多字節字符的正確性，特別是在處理 UTF-8 編碼的文件時。