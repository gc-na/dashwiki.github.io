# [台灣] Debian Almquist Shell (dash) export 使用法: 設定環境變數

## Overview
`export` 命令用於設定環境變數，使其在當前 shell 及其子進程中可用。這對於配置系統環境或傳遞參數給其他程序非常有用。

## Usage
基本語法如下：
```
export [options] [arguments]
```

## Common Options
- `-n`：取消對指定變數的導出。
- `-p`：顯示所有導出的變數及其值。

## Common Examples

1. 導出一個變數：
   ```sh
   MY_VAR="Hello, World!"
   export MY_VAR
   ```

2. 導出多個變數：
   ```sh
   export VAR1="Value1" VAR2="Value2"
   ```

3. 查看所有導出的變數：
   ```sh
   export -p
   ```

4. 取消導出一個變數：
   ```sh
   export -n MY_VAR
   ```

## Tips
- 確保在導出變數之前先為其賦值，否則導出的變數將不會有任何值。
- 使用 `export -p` 可以快速檢查當前所有導出的環境變數，這對於調試非常有幫助。
- 將常用的環境變數導出到 `.profile` 或 `.bashrc` 文件中，這樣每次啟動 shell 時都會自動加載。