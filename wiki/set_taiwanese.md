# [台灣] Debian Almquist Shell (dash) set 使用法: 設定環境變數和選項

## Overview
`set` 命令用於設定或顯示當前 shell 的選項和變數。這個命令可以幫助用戶控制 shell 的行為，並且能夠設置環境變數。

## Usage
基本語法如下：
```
set [options] [arguments]
```

## Common Options
- `-e`: 當命令執行失敗時，立即退出。
- `-u`: 在使用未設定的變數時，顯示錯誤。
- `-x`: 在執行命令之前，顯示命令及其參數。
- `+o`: 取消某個選項，例如 `+e` 會取消 `-e` 的效果。

## Common Examples
1. 設定 shell 在遇到錯誤時退出：
   ```sh
   set -e
   ```

2. 顯示所有變數和選項：
   ```sh
   set
   ```

3. 開啟追蹤模式，顯示每個執行的命令：
   ```sh
   set -x
   ```

4. 設定一個環境變數：
   ```sh
   MY_VAR="Hello, World!"
   ```

5. 使用 `-u` 來檢查未設定的變數：
   ```sh
   set -u
   echo $UNSET_VAR  # 這會導致錯誤
   ```

## Tips
- 在腳本的開頭使用 `set -e` 可以幫助捕捉錯誤，避免後續命令在錯誤發生後繼續執行。
- 使用 `set -u` 可以幫助避免因為拼寫錯誤而導致的未定義變數問題。
- 在調試腳本時，使用 `set -x` 可以讓你看到每一步的執行過程，方便找出問題。