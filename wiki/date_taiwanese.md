# [台灣] Debian Almquist Shell (dash) date 日期: 顯示或設定日期和時間

## Overview
`date` 命令用於顯示或設定系統的日期和時間。它可以以多種格式輸出當前的日期和時間，並且還可以用來設置系統的日期和時間。

## Usage
基本語法如下：
```
date [options] [arguments]
```

## Common Options
- `-u`：以協調世界時間（UTC）顯示日期和時間。
- `+FORMAT`：自定義輸出格式，FORMAT 是一個格式字符串。
- `-s STRING`：設定系統的日期和時間，STRING 是所需的日期和時間字符串。

## Common Examples
- 顯示當前日期和時間：
  ```bash
  date
  ```

- 以 UTC 顯示當前日期和時間：
  ```bash
  date -u
  ```

- 自定義格式顯示日期：
  ```bash
  date "+%Y-%m-%d %H:%M:%S"
  ```

- 設定系統日期和時間：
  ```bash
  date -s "2023-10-01 12:00:00"
  ```

## Tips
- 使用 `+FORMAT` 時，可以參考 `man date` 來了解可用的格式選項。
- 設定系統時間需要管理員權限，確保你有適當的權限來執行此操作。
- 在使用 `date -s` 設定時間之前，建議先檢查當前時間，以避免不必要的錯誤。