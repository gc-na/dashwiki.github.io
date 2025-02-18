# [台灣] Debian Almquist Shell (dash) wget 用法: 下載檔案的工具

## Overview
`wget` 是一個用於從網路上下載檔案的命令行工具。它支援 HTTP、HTTPS 和 FTP 協議，並且可以在不需要使用者介面的情況下進行下載，這使得它非常適合自動化任務和批量下載。

## Usage
基本語法如下：
```
wget [options] [arguments]
```

## Common Options
- `-O <file>`: 指定下載後的檔案名稱。
- `-q`: 啟用安靜模式，下載過程中不顯示任何輸出。
- `-c`: 繼續未完成的下載。
- `--limit-rate=<rate>`: 限制下載速度，例如 `--limit-rate=200k`。
- `-r`: 進行遞迴下載，適合下載整個網站。

## Common Examples
以下是一些常見的使用範例：

1. 下載單一檔案：
   ```bash
   wget http://example.com/file.zip
   ```

2. 下載並指定檔案名稱：
   ```bash
   wget -O myfile.zip http://example.com/file.zip
   ```

3. 繼續未完成的下載：
   ```bash
   wget -c http://example.com/largefile.zip
   ```

4. 下載整個網站：
   ```bash
   wget -r http://example.com
   ```

5. 限制下載速度：
   ```bash
   wget --limit-rate=100k http://example.com/file.zip
   ```

## Tips
- 使用 `-q` 選項可以在自動化腳本中減少輸出，讓日誌更乾淨。
- 當下載大檔案時，考慮使用 `-c` 選項，以便在網路中斷後可以繼續下載。
- 在下載整個網站時，請注意網站的使用條款，避免對伺服器造成過大負擔。