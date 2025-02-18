# [台灣] Debian Almquist Shell (dash) find 使用方式: 尋找檔案名稱

## Overview
`find` 命令用於在檔案系統中搜尋符合特定條件的檔案和目錄。它可以根據名稱、大小、修改時間等多種條件進行搜尋，並支援遞迴搜尋。

## Usage
基本語法如下：
```
find [選項] [參數]
```

## Common Options
- `-name <pattern>`: 根據檔案名稱匹配搜尋。
- `-type <type>`: 根據檔案類型搜尋，例如 `f` 代表檔案，`d` 代表目錄。
- `-size <n>`: 根據檔案大小搜尋，`n` 可以是數字加上單位（如 `k`、`M`）。
- `-mtime <n>`: 根據檔案的最後修改時間搜尋，`n` 可以是正數或負數。
- `-exec <command> {} \;`: 對找到的每個檔案執行指定的命令。

## Common Examples
- 根據名稱搜尋所有 `.txt` 檔案：
  ```bash
  find . -name "*.txt"
  ```

- 尋找所有目錄：
  ```bash
  find /path/to/search -type d
  ```

- 尋找大小超過 1MB 的檔案：
  ```bash
  find . -size +1M
  ```

- 尋找最近 7 天內修改過的檔案：
  ```bash
  find . -mtime -7
  ```

- 對找到的檔案執行 `ls -l` 命令：
  ```bash
  find . -name "*.log" -exec ls -l {} \;
  ```

## Tips
- 使用 `-print` 選項可以顯示找到的檔案，這是 `find` 的預設行為。
- 結合 `-type` 和 `-name` 可以更精確地搜尋特定類型的檔案。
- 使用 `-maxdepth` 限制搜尋的目錄深度，避免搜尋過多不必要的目錄。