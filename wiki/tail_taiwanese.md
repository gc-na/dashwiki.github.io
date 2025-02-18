# [台灣] Debian Almquist Shell (dash) tail 使用法: 查看檔案結尾的內容

## Overview
`tail` 命令用於顯示檔案的最後幾行內容，這在查看日誌檔案或追蹤檔案變更時特別有用。

## Usage
基本語法如下：
```
tail [選項] [檔案]
```

## Common Options
- `-n <數字>`: 顯示檔案的最後 <數字> 行，預設為 10 行。
- `-f`: 持續追蹤檔案的新增內容，適合用於即時監控日誌檔案。
- `-c <數字>`: 顯示檔案的最後 <數字> 字元。

## Common Examples
顯示檔案的最後 10 行：
```sh
tail myfile.txt
```

顯示檔案的最後 20 行：
```sh
tail -n 20 myfile.txt
```

持續追蹤日誌檔案的新增內容：
```sh
tail -f /var/log/syslog
```

顯示檔案的最後 50 字元：
```sh
tail -c 50 myfile.txt
```

## Tips
- 使用 `tail -f` 來即時監控日誌檔案的變化，這對於除錯非常有幫助。
- 結合 `grep` 使用，可以過濾出特定的關鍵字，例如：
  ```sh
  tail -f /var/log/syslog | grep "error"
  ```
- 若要查看多個檔案的最後幾行，可以將檔案名稱一起列出：
  ```sh
  tail file1.txt file2.txt
  ```