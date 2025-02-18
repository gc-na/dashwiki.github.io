# [台灣] Debian Almquist Shell (dash) chmod 使用方式: 調整檔案權限

## Overview
`chmod` 命令用於改變檔案或目錄的存取權限。透過這個命令，使用者可以設定誰可以讀取、寫入或執行特定的檔案。

## Usage
基本語法如下：
```
chmod [選項] [參數]
```

## Common Options
- `-R`：遞迴地改變目錄及其內容的權限。
- `-v`：顯示每個檔案的變更情況。
- `-c`：僅顯示有變更的檔案。

## Common Examples
1. **設定檔案為可執行**
   ```bash
   chmod +x myscript.sh
   ```

2. **設定檔案的讀取和寫入權限**
   ```bash
   chmod 664 myfile.txt
   ```

3. **遞迴改變目錄及其內容的權限**
   ```bash
   chmod -R 755 mydirectory/
   ```

4. **顯示變更的檔案**
   ```bash
   chmod -v 600 myprivatefile.txt
   ```

## Tips
- 使用數字模式（如 755、644）可以更快速地設定權限。
- 在改變權限之前，建議先檢查當前的權限設定，使用 `ls -l` 命令。
- 小心使用 `-R` 選項，因為它會影響所有子目錄和檔案。