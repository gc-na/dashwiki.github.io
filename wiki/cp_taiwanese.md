# [台灣] Debian Almquist Shell (dash) cp 用法: 複製檔案和目錄

## Overview
`cp` 命令用於複製檔案和目錄。它可以將一個或多個檔案從一個位置複製到另一個位置，並且可以選擇性地保留檔案的屬性。

## Usage
基本語法如下：
```bash
cp [選項] [來源] [目標]
```

## Common Options
- `-r`：遞迴複製目錄及其內容。
- `-i`：在覆蓋檔案之前提示用戶確認。
- `-u`：僅複製來源檔案比目標檔案更新的檔案。
- `-v`：顯示詳細的複製過程。

## Common Examples
1. 複製單個檔案：
   ```bash
   cp file1.txt file2.txt
   ```

2. 複製並覆蓋檔案（無提示）：
   ```bash
   cp -f file1.txt file2.txt
   ```

3. 遞迴複製目錄：
   ```bash
   cp -r dir1/ dir2/
   ```

4. 複製檔案並顯示過程：
   ```bash
   cp -v file1.txt file2.txt
   ```

5. 僅複製更新的檔案：
   ```bash
   cp -u file1.txt file2.txt
   ```

## Tips
- 使用 `-i` 選項可以避免意外覆蓋重要檔案。
- 在複製大型目錄時，考慮使用 `-v` 來監控進度。
- 當需要保留檔案屬性時，可以使用 `-p` 選項。