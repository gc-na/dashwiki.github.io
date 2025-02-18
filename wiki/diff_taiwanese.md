# [台灣] Debian Almquist Shell (dash) diff 用法: 比較檔案差異

## Overview
`diff` 命令用於比較兩個檔案的內容，並顯示它們之間的差異。這對於開發者和系統管理員來說非常有用，可以幫助他們了解檔案的變更情況。

## Usage
基本語法如下：
```
diff [選項] [檔案1] [檔案2]
```

## Common Options
- `-u`：以統一格式顯示差異，這種格式更易於閱讀。
- `-c`：以上下文格式顯示差異，提供更多的上下文資訊。
- `-i`：忽略大小寫的差異。
- `-w`：忽略空白字符的差異。

## Common Examples
以下是一些常見的 `diff` 使用範例：

1. 比較兩個檔案的內容：
   ```sh
   diff file1.txt file2.txt
   ```

2. 以統一格式顯示差異：
   ```sh
   diff -u file1.txt file2.txt
   ```

3. 以上下文格式顯示差異：
   ```sh
   diff -c file1.txt file2.txt
   ```

4. 忽略大小寫的差異：
   ```sh
   diff -i file1.txt file2.txt
   ```

5. 忽略空白字符的差異：
   ```sh
   diff -w file1.txt file2.txt
   ```

## Tips
- 在使用 `diff` 時，建議使用 `-u` 或 `-c` 選項，因為這樣可以讓差異更清晰易懂。
- 可以將 `diff` 的輸出重定向到檔案中，方便後續查看：
  ```sh
  diff file1.txt file2.txt > differences.txt
  ```
- 若要比較目錄中的所有檔案，可以使用 `diff -r` 選項：
  ```sh
  diff -r dir1/ dir2/
  ```