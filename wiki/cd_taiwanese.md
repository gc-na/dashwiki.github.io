# [台灣] Debian Almquist Shell (dash) cd 使用法: 切換目錄

## Overview
`cd` 命令用於改變當前工作目錄。這是一個基本的命令，幫助使用者在檔案系統中導航。

## Usage
基本語法如下：
```
cd [選項] [參數]
```

## Common Options
- `-P`：使用物理路徑，避免符號鏈接。
- `-L`：使用邏輯路徑，這是預設行為。

## Common Examples
1. 切換到家目錄：
   ```sh
   cd ~
   ```

2. 切換到上層目錄：
   ```sh
   cd ..
   ```

3. 切換到指定的目錄：
   ```sh
   cd /path/to/directory
   ```

4. 使用相對路徑切換目錄：
   ```sh
   cd ./subdirectory
   ```

5. 切換到最後一次訪問的目錄：
   ```sh
   cd -
   ```

## Tips
- 使用 `cd ~` 可以快速返回到家目錄。
- 使用 `cd ..` 可以方便地向上導航。
- 確保目錄存在，否則 `cd` 會顯示錯誤訊息。