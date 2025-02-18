# [台灣] Debian Almquist Shell (dash) renice 用法: 調整進程優先權

## Overview
`renice` 命令用於調整正在運行的進程的優先權。通過改變進程的優先級，使用者可以控制進程在系統資源分配中的優先順序，從而影響其執行性能。

## Usage
基本語法如下：
```
renice [options] [arguments]
```

## Common Options
- `-n, --priority <number>`: 指定新的優先權值，範圍通常是 -20（最高優先權）到 19（最低優先權）。
- `-p, --pid <pid>`: 指定要調整的進程 ID。
- `-g, --pgroup <pgrp>`: 指定要調整的進程組 ID。
- `-u, --user <user>`: 指定要調整的用戶的所有進程。

## Common Examples
1. 調整特定進程的優先權：
   ```bash
   renice -n 10 -p 1234
   ```
   這條命令將進程 ID 為 1234 的進程優先權設置為 10。

2. 調整某用戶的所有進程優先權：
   ```bash
   renice -n -5 -u username
   ```
   這條命令將用戶 `username` 的所有進程優先權設置為 -5。

3. 調整進程組的優先權：
   ```bash
   renice -n 15 -g 5678
   ```
   這條命令將進程組 ID 為 5678 的所有進程優先權設置為 15。

## Tips
- 在使用 `renice` 調整優先權時，請確保擁有足夠的權限，某些優先權調整可能需要超級用戶權限。
- 使用 `ps` 命令查看當前進程的優先權，以便選擇合適的優先權值進行調整。
- 適當調整進程優先權可以改善系統性能，但過度調整可能會導致系統不穩定。