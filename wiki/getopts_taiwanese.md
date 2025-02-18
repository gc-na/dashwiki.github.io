# [台灣] Debian Almquist Shell (dash) getopts 使用方式: 解析選項的工具

## Overview
`getopts` 是一個用於解析命令行選項的工具，特別適合在 shell 腳本中使用。它可以幫助開發者輕鬆地處理短選項（例如 `-a`、`-b`）和其對應的參數。

## Usage
基本語法如下：
```sh
getopts optstring variable
```

## Common Options
- `optstring`: 一個字串，定義可接受的選項。每個選項字母代表一個選項，若選項需要參數，則在字母後加上冒號（例如 `a:`）。
- `variable`: 用於存儲當前解析的選項的變數名稱。

## Common Examples

### 基本範例
以下是一個簡單的範例，展示如何使用 `getopts` 解析選項：
```sh
#!/bin/sh
while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "選項 a 被選擇"
      ;;
    b)
      echo "選項 b 的參數是: $OPTARG"
      ;;
    c)
      echo "選項 c 的參數是: $OPTARG"
      ;;
    *)
      echo "無效的選項"
      ;;
  esac
done
```

### 使用選項
假設我們將上述腳本保存為 `script.sh`，可以這樣運行：
```sh
sh script.sh -a -b 123 -c "Hello"
```
輸出將會是：
```
選項 a 被選擇
選項 b 的參數是: 123
選項 c 的參數是: Hello
```

### 處理無效選項
如果使用無效選項，則會顯示錯誤訊息：
```sh
sh script.sh -x
```
輸出將會是：
```
無效的選項
```

## Tips
- 確保在 `optstring` 中正確地定義選項及其參數需求。
- 使用 `OPTARG` 變數來獲取選項的參數值。
- 在腳本中使用 `getopts` 時，最好將選項解析放在 `while` 迴圈中，以便處理多個選項。