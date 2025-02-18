# [台灣] Debian Almquist Shell (dash) bzip2 使用法: 壓縮和解壓縮檔案

## Overview
bzip2 是一個用於壓縮和解壓縮檔案的命令行工具，能有效地減少檔案的大小，特別適合大型檔案的處理。

## Usage
基本語法如下：
```
bzip2 [options] [arguments]
```

## Common Options
- `-d` 或 `--decompress`: 解壓縮檔案。
- `-k` 或 `--keep`: 在壓縮或解壓縮後保留原始檔案。
- `-f` 或 `--force`: 強制壓縮或解壓縮，即使檔案已存在。
- `-v` 或 `--verbose`: 顯示詳細的操作過程。

## Common Examples
- 壓縮檔案：
  ```bash
  bzip2 example.txt
  ```
  這會將 `example.txt` 壓縮為 `example.txt.bz2`。

- 解壓縮檔案：
  ```bash
  bzip2 -d example.txt.bz2
  ```
  這會將 `example.txt.bz2` 解壓縮回 `example.txt`。

- 保留原始檔案：
  ```bash
  bzip2 -k example.txt
  ```
  這會壓縮 `example.txt`，並保留原始檔案。

- 強制壓縮已存在的檔案：
  ```bash
  bzip2 -f example.txt
  ```
  如果 `example.txt.bz2` 已存在，這會覆蓋它。

## Tips
- 使用 `-v` 選項可以幫助你了解壓縮的進度和結果。
- 對於非常大的檔案，考慮使用 `-k` 選項，以免意外刪除原始檔案。
- 如果你需要解壓縮多個檔案，可以使用通配符，例如：
  ```bash
  bzip2 -d *.bz2
  ```