# [台灣] Debian Almquist Shell (dash) unzip 用法: 解壓縮檔案

## Overview
`unzip` 命令用於解壓縮 ZIP 格式的檔案。這個命令可以讓使用者輕鬆地將壓縮的檔案內容提取到指定的目錄中。

## Usage
基本語法如下：
```sh
unzip [選項] [檔案]
```

## Common Options
- `-d <目錄>`: 指定解壓縮的目錄。
- `-l`: 列出 ZIP 檔案中的內容，但不進行解壓縮。
- `-o`: 自動覆蓋已存在的檔案而不提示。
- `-q`: 安靜模式，不顯示解壓縮過程中的詳細信息。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮檔案到當前目錄：
   ```sh
   unzip example.zip
   ```

2. 解壓縮檔案到指定的目錄：
   ```sh
   unzip example.zip -d /path/to/directory
   ```

3. 列出 ZIP 檔案的內容：
   ```sh
   unzip -l example.zip
   ```

4. 自動覆蓋已存在的檔案：
   ```sh
   unzip -o example.zip
   ```

5. 在安靜模式下解壓縮檔案：
   ```sh
   unzip -q example.zip
   ```

## Tips
- 確保在解壓縮之前有足夠的磁碟空間，特別是對於大型 ZIP 檔案。
- 使用 `-d` 選項可以避免將檔案解壓縮到當前工作目錄，這樣可以更好地組織檔案。
- 如果不確定 ZIP 檔案的內容，先使用 `-l` 選項查看，這樣可以避免不必要的解壓縮。