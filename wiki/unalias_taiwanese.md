# [台灣] Debian Almquist Shell (dash) unalias 使用法: 移除別名

## Overview
`unalias` 命令用於刪除已設定的命令別名。這對於清除不再需要的別名或恢復命令的原始行為非常有用。

## Usage
基本語法如下：
```sh
unalias [options] [arguments]
```

## Common Options
- `-a`：刪除所有的別名。
- `-m`：顯示所有的別名。

## Common Examples
以下是一些實用的範例：

1. 刪除單一別名：
   ```sh
   unalias ll
   ```

2. 刪除多個別名：
   ```sh
   unalias ll rm
   ```

3. 刪除所有別名：
   ```sh
   unalias -a
   ```

4. 檢查當前別名（使用 `alias` 命令）：
   ```sh
   alias
   ```

## Tips
- 在使用 `unalias` 之前，可以先使用 `alias` 命令檢查目前的別名設定。
- 若要保持環境的整潔，建議定期檢查並移除不再需要的別名。
- 可以在啟動腳本中使用 `unalias` 來確保每次啟動時不會載入不需要的別名。