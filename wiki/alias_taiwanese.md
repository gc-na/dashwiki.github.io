# [台灣] Debian Almquist Shell (dash) alias 用法: 簡化命令

## Overview
`alias` 命令用來為長命令或常用命令創建簡短的別名，這樣可以提高效率並減少輸入的工作量。

## Usage
基本語法如下：
```sh
alias [options] [arguments]
```

## Common Options
- `-p`：顯示當前所有的別名。
- `name=value`：創建一個新的別名，`name` 是別名的名稱，`value` 是要執行的命令。

## Common Examples
1. 創建一個簡單的別名：
   ```sh
   alias ll='ls -la'
   ```
   這樣以後輸入 `ll` 就會執行 `ls -la` 命令。

2. 查看當前所有別名：
   ```sh
   alias -p
   ```

3. 創建一個別名來更新系統：
   ```sh
   alias update='sudo apt update && sudo apt upgrade'
   ```
   這樣輸入 `update` 就會執行更新命令。

4. 移除一個別名：
   ```sh
   unalias ll
   ```
   這樣會刪除之前創建的 `ll` 別名。

## Tips
- 在你的 `.dashrc` 或 `.profile` 文件中添加別名，這樣每次啟動 shell 時都會自動加載。
- 使用有意義的別名，以便於記憶和使用。
- 避免與系統命令重名，以免造成混淆。