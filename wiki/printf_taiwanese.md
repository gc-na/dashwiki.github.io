# [台灣] Debian Almquist Shell (dash) printf 使用方法: 格式化輸出文本

## Overview
`printf` 命令用於格式化輸出文本，類似於 C 語言中的 `printf` 函數。它可以根據指定的格式將數據輸出到標準輸出。

## Usage
基本語法如下：
```sh
printf [options] [arguments]
```

## Common Options
- `-v var`: 將格式化的輸出存儲到變數 `var` 中，而不是直接輸出。
- `--help`: 顯示幫助信息。
- `--version`: 顯示版本信息。

## Common Examples
1. **基本文本輸出**
   ```sh
   printf "Hello, World!\n"
   ```

2. **格式化數字**
   ```sh
   printf "Number: %d\n" 42
   ```

3. **浮點數格式化**
   ```sh
   printf "Pi: %.2f\n" 3.14159
   ```

4. **多個變量輸出**
   ```sh
   printf "Name: %s, Age: %d\n" "Alice" 30
   ```

5. **將輸出存儲到變數**
   ```sh
   printf -v my_var "Value: %s" "Hello"
   echo $my_var
   ```

## Tips
- 使用 `\n` 來換行，讓輸出更整齊。
- 格式化字符串中的佔位符（如 `%s`, `%d`, `%f`）可以幫助你控制輸出的格式。
- 測試不同的格式化選項，了解如何最佳化你的輸出。