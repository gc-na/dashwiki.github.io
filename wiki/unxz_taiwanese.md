# [台灣] Debian Almquist Shell (dash) unxz 使用法: 解壓縮 .xz 檔案

## Overview
`unxz` 是一個用來解壓縮 `.xz` 格式檔案的命令。這個命令可以將壓縮的檔案恢復到原始狀態，方便使用者存取檔案內容。

## Usage
基本語法如下：
```
unxz [選項] [檔案]
```

## Common Options
- `-k`：保留原始的壓縮檔案。
- `-f`：強制解壓縮，即使檔案已經存在。
- `-v`：顯示詳細的解壓縮過程。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮單一檔案：
   ```bash
   unxz example.xz
   ```

2. 解壓縮並保留原始檔案：
   ```bash
   unxz -k example.xz
   ```

3. 強制解壓縮已存在的檔案：
   ```bash
   unxz -f example.xz
   ```

4. 解壓縮並顯示詳細過程：
   ```bash
   unxz -v example.xz
   ```

## Tips
- 在解壓縮之前，確認檔案的完整性，以避免損壞的檔案導致解壓縮失敗。
- 使用 `-k` 選項可以保留原始檔案，這在需要多次解壓縮時特別有用。
- 如果不確定檔案是否已經存在，可以先使用 `ls` 命令檢查，避免不必要的覆蓋。