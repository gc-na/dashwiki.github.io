# [台灣] Debian Almquist Shell (dash) dirname 用法: 提取路徑中的目錄名稱

## Overview
`dirname` 命令用於從給定的路徑中提取目錄名稱。它會返回路徑中最後一個斜線之前的部分，這對於處理文件路徑時非常有用。

## Usage
基本語法如下：
```
dirname [options] [arguments]
```

## Common Options
- `-z`：以空字元作為分隔符輸出，適用於處理包含空格的路徑。
- `--help`：顯示幫助信息。
- `--version`：顯示版本信息。

## Common Examples
以下是一些常見的使用範例：

1. 提取單個路徑的目錄名稱：
   ```sh
   dirname /home/user/document.txt
   ```
   輸出：
   ```
   /home/user
   ```

2. 處理多個路徑：
   ```sh
   dirname /var/log/syslog /usr/local/bin/script.sh
   ```
   輸出：
   ```
   /var/log
   /usr/local/bin
   ```

3. 使用空字元作為分隔符：
   ```sh
   dirname -z "/home/user/my documents/file.txt"
   ```
   輸出：
   ```
   /home/user/my documents
   ```

## Tips
- 使用 `dirname` 配合其他命令，如 `basename`，可以更靈活地處理路徑。
- 在腳本中使用 `dirname` 時，確保處理好路徑的結尾斜線，以避免意外的結果。
- 當處理多個路徑時，可以將結果重定向到文件中，方便後續使用。