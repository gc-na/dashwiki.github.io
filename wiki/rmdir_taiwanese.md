# [台灣] Debian Almquist Shell (dash) rmdir 使用方法: 刪除空目錄

## Overview
`rmdir` 命令用於刪除空的目錄。如果目錄內有檔案或其他目錄，則無法使用此命令刪除。

## Usage
基本語法如下：
```
rmdir [選項] [參數]
```

## Common Options
- `-p`：同時刪除指定目錄的父目錄，前提是這些父目錄也是空的。
- `--ignore-fail-on-non-empty`：忽略非空目錄的錯誤，這樣即使目錄不空也不會報錯。

## Common Examples
1. 刪除一個空目錄：
   ```bash
   rmdir my_empty_directory
   ```

2. 同時刪除空目錄及其父目錄：
   ```bash
   rmdir -p my_empty_directory/parent_directory
   ```

3. 忽略非空目錄的錯誤：
   ```bash
   rmdir --ignore-fail-on-non-empty my_non_empty_directory
   ```

## Tips
- 在使用 `rmdir` 之前，請確保目錄是空的，以避免錯誤。
- 使用 `-p` 選項時，請確認父目錄也是空的，否則將無法刪除。
- 可以使用 `ls` 命令檢查目錄是否為空。