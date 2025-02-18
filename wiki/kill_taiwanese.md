# [台灣] Debian Almquist Shell (dash) kill 使用說明: 終止進程

## Overview
`kill` 命令用於終止正在運行的進程。它可以通過進程ID（PID）來指定要終止的進程，並且可以發送不同的信號來控制進程的行為。

## Usage
基本語法如下：
```
kill [選項] [參數]
```

## Common Options
- `-l`：列出所有可用的信號名稱。
- `-s SIGNAL`：指定要發送的信號，SIGNAL 可以是信號名稱或數字。
- `-n`：使用信號的數字編號來終止進程。

## Common Examples
1. 終止指定 PID 的進程：
   ```bash
   kill 1234
   ```

2. 強制終止進程（使用 `-9` 信號）：
   ```bash
   kill -9 1234
   ```

3. 列出所有可用的信號：
   ```bash
   kill -l
   ```

4. 使用信號名稱終止進程：
   ```bash
   kill -s TERM 1234
   ```

## Tips
- 在使用 `kill` 命令時，確保你有足夠的權限來終止該進程。
- 使用 `kill -9` 時要小心，因為這會強制終止進程，可能會導致數據丟失。
- 可以使用 `ps` 命令來查找進程的 PID，然後再使用 `kill` 來終止它。