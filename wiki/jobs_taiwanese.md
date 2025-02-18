# [台灣] Debian Almquist Shell (dash) jobs 使用法: 管理背景工作

## Overview
`jobs` 命令用於顯示當前 shell 中的背景工作狀態。這些工作可以是暫停或正在運行的進程，幫助用戶管理和監控他們的任務。

## Usage
基本語法如下：
```
jobs [options] [arguments]
```

## Common Options
- `-l`：顯示每個工作對應的進程 ID。
- `-n`：僅顯示最近狀態改變的工作。
- `-p`：僅顯示進程 ID，而不顯示其他信息。

## Common Examples
以下是一些常見的用法示例：

1. 顯示所有背景工作：
   ```sh
   jobs
   ```

2. 顯示背景工作及其進程 ID：
   ```sh
   jobs -l
   ```

3. 僅顯示最近狀態改變的工作：
   ```sh
   jobs -n
   ```

4. 僅顯示進程 ID：
   ```sh
   jobs -p
   ```

## Tips
- 在啟動長時間運行的任務時，可以使用 `&` 將其放入背景，然後使用 `jobs` 來檢查狀態。
- 如果需要將某個背景工作帶回前台，可以使用 `fg %job_number`，其中 `job_number` 是 `jobs` 命令顯示的工作編號。
- 定期檢查背景工作狀態，確保沒有意外的進程在運行，特別是在執行多個任務時。