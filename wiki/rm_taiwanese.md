# [台灣] Debian Almquist Shell (dash) rm 用法: 刪除檔案或目錄

## Overview
`rm` 命令用於刪除檔案或目錄。這是一個強大的工具，能夠永久移除指定的檔案，並且不會將它們放入回收桶。

## Usage
基本語法如下：
```
rm [options] [arguments]
```

## Common Options
- `-f`：強制刪除檔案，無需提示。
- `-i`：在刪除每個檔案之前要求確認。
- `-r`：遞迴刪除目錄及其內容。
- `-v`：顯示刪除過程中的詳細信息。

## Common Examples
- 刪除單個檔案：
  ```bash
  rm file.txt
  ```

- 強制刪除檔案：
  ```bash
  rm -f file.txt
  ```

- 刪除目錄及其內容：
  ```bash
  rm -r directory_name
  ```

- 在刪除之前要求確認：
  ```bash
  rm -i file.txt
  ```

- 刪除多個檔案：
  ```bash
  rm file1.txt file2.txt file3.txt
  ```

## Tips
- 使用 `-i` 選項可以防止意外刪除重要檔案。
- 在刪除目錄之前，確保你真的想要刪除其所有內容，因為這個操作是不可逆的。
- 定期備份重要檔案，以防不小心刪除。