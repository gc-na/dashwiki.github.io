# [台灣] Debian Almquist Shell (dash) mv 用法: [移動或重新命名檔案]

## Overview
`mv` 命令用於在檔案系統中移動檔案或目錄，或是重新命名它們。這個命令非常實用，尤其是在需要整理檔案或更改檔案名稱時。

## Usage
基本語法如下：
```bash
mv [選項] [來源] [目標]
```

## Common Options
- `-i`：在覆蓋檔案之前提示使用者確認。
- `-u`：僅在來源檔案較新或目標檔案不存在時移動檔案。
- `-v`：顯示詳細的操作過程，讓使用者知道正在進行哪些動作。

## Common Examples
1. **移動檔案**
   ```bash
   mv file.txt /path/to/destination/
   ```
   這個命令將 `file.txt` 移動到指定的目錄。

2. **重新命名檔案**
   ```bash
   mv oldname.txt newname.txt
   ```
   這個命令將 `oldname.txt` 重新命名為 `newname.txt`。

3. **使用 -i 選項以防止覆蓋**
   ```bash
   mv -i file.txt /path/to/destination/
   ```
   如果目標目錄中已經存在同名檔案，這個命令會提示使用者確認是否要覆蓋。

4. **使用 -u 選項僅移動較新檔案**
   ```bash
   mv -u file.txt /path/to/destination/
   ```
   這個命令只會在 `file.txt` 比目標目錄中的同名檔案更新時才進行移動。

## Tips
- 在移動大量檔案時，可以使用通配符（如 `*`）來選擇多個檔案。
- 使用 `-v` 選項可以幫助你了解命令的執行過程，特別是在處理多個檔案時。
- 在進行重要的檔案移動或重新命名操作時，建議先備份檔案以防不測。