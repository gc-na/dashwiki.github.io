# [台灣] Debian Almquist Shell (dash) whoami 用法: 獲取當前使用者名稱

## Overview
`whoami` 命令用於顯示當前登錄的使用者名稱。這對於確認你正在以哪個使用者身份執行命令非常有用。

## Usage
基本語法如下：
```
whoami [options] [arguments]
```

## Common Options
- `--help`：顯示幫助信息，列出所有可用選項。
- `--version`：顯示版本信息。

## Common Examples
以下是幾個常見的使用範例：

1. 獲取當前使用者名稱：
   ```sh
   whoami
   ```

2. 獲取當前使用者名稱並顯示幫助信息：
   ```sh
   whoami --help
   ```

3. 獲取當前使用者名稱並顯示版本信息：
   ```sh
   whoami --version
   ```

## Tips
- 使用 `whoami` 可以快速檢查你是否以預期的使用者身份運行命令，特別是在使用 sudo 或 su 切換使用者後。
- 將 `whoami` 與其他命令結合使用，可以自動化腳本中的使用者檢查。