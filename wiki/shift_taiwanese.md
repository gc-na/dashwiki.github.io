# [台灣] Debian Almquist Shell (dash) shift 用法: 調整位置參數

## Overview
`shift` 命令用於調整位置參數，這意味著它可以改變腳本中參數的索引，讓後續的參數可以更方便地訪問。

## Usage
基本語法如下：
```
shift [n]
```
其中 `n` 是要移動的參數數量，預設為 1。

## Common Options
- `n`：指定要移動的參數數量，預設為 1。如果指定 `n`，則會將位置參數向左移動 `n` 個位置。

## Common Examples

### 基本用法
將位置參數向左移動一個位置：
```sh
#!/bin/dash
set -- one two three
echo "$1"  # 輸出: one
shift
echo "$1"  # 輸出: two
```

### 移動多個位置
將位置參數向左移動兩個位置：
```sh
#!/bin/dash
set -- apple banana cherry date
echo "$1"  # 輸出: apple
shift 2
echo "$1"  # 輸出: cherry
```

### 在循環中使用
在循環中使用 `shift` 來處理所有位置參數：
```sh
#!/bin/dash
set -- first second third fourth
while [ "$#" -gt 0 ]; do
    echo "$1"
    shift
done
```

## Tips
- 在使用 `shift` 時，確保你知道當前的位置參數數量，以避免意外移動過多的位置。
- 使用 `shift` 可以簡化處理多個參數的邏輯，特別是在需要循環處理時。
- 結合 `getopts` 使用 `shift` 可以更有效地解析命令行選項。