# [台灣] Debian Almquist Shell (dash) strace 使用法: 追蹤系統呼叫

## Overview
`strace` 是一個強大的工具，用於追蹤程序執行過程中所發出的系統呼叫和接收的信號。這對於除錯和性能分析非常有幫助，因為它能夠顯示程序與內核之間的互動。

## Usage
基本語法如下：
```bash
strace [options] [arguments]
```

## Common Options
- `-c`: 總結系統呼叫的統計信息。
- `-e trace=<set>`: 指定要追蹤的系統呼叫類型。
- `-p <pid>`: 附加到已存在的進程，根據其進程ID進行追蹤。
- `-o <file>`: 將輸出寫入指定的文件，而不是標準輸出。

## Common Examples
1. 追蹤一個簡單的命令：
   ```bash
   strace ls
   ```

2. 追蹤特定的系統呼叫，例如 `open` 和 `close`：
   ```bash
   strace -e trace=open,close ls
   ```

3. 附加到一個正在運行的進程，假設進程ID是1234：
   ```bash
   strace -p 1234
   ```

4. 將輸出寫入文件：
   ```bash
   strace -o output.txt ls
   ```

5. 總結系統呼叫的統計信息：
   ```bash
   strace -c ls
   ```

## Tips
- 使用 `-o` 選項可以方便地保存輸出，便於後續分析。
- 當追蹤大型程序時，考慮使用 `-c` 來獲取統計信息，這樣可以快速了解哪些系統呼叫最常被使用。
- 在進行性能分析時，注意觀察系統呼叫的延遲，這能幫助你找到潛在的瓶頸。