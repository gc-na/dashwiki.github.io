# [台灣] Debian Almquist Shell (dash) rsync 使用法: 檔案同步工具

## Overview
`rsync` 是一個強大的檔案同步工具，主要用於在本地或遠端系統之間高效地複製和同步檔案。它能夠只傳輸變更的部分，從而節省帶寬和時間。

## Usage
基本語法如下：
```
rsync [options] [arguments]
```

## Common Options
- `-a`：以歸檔模式運行，這會保留檔案的屬性（如權限、時間戳等）。
- `-v`：顯示詳細的輸出，讓使用者可以看到正在進行的操作。
- `-z`：在傳輸過程中進行壓縮，適合於網路帶寬有限的情況。
- `-r`：遞迴地複製目錄及其內容。
- `--delete`：在目標位置刪除源位置不存在的檔案，保持兩者一致。

## Common Examples
以下是一些常見的 `rsync` 使用範例：

1. 將本地目錄同步到遠端伺服器：
   ```bash
   rsync -avz /local/directory/ user@remote:/remote/directory/
   ```

2. 從遠端伺服器下載檔案到本地：
   ```bash
   rsync -avz user@remote:/remote/directory/ /local/directory/
   ```

3. 遞迴複製目錄並刪除目標中不存在的檔案：
   ```bash
   rsync -av --delete /local/directory/ user@remote:/remote/directory/
   ```

4. 僅傳輸檔案的變更部分：
   ```bash
   rsync -av /local/directory/ user@remote:/remote/directory/
   ```

## Tips
- 使用 `-n` 或 `--dry-run` 選項可以在實際執行之前模擬操作，這樣可以避免意外的檔案刪除或覆蓋。
- 定期備份重要資料時，考慮使用 `--delete` 選項，但要小心使用，以免刪除不應該刪除的檔案。
- 結合 `cron` 定時任務可以自動化檔案同步，確保資料的即時更新。