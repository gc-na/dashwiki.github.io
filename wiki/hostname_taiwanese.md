# [台灣] Debian Almquist Shell (dash) hostname 用法: 查詢或設定主機名稱

## Overview
`hostname` 命令用於顯示或設定系統的主機名稱。主機名稱是用來識別網絡上的設備，對於網絡管理和系統配置非常重要。

## Usage
基本語法如下：
```
hostname [options] [arguments]
```

## Common Options
- `-f`：顯示完整的主機名稱（FQDN）。
- `-i`：顯示主機的 IP 地址。
- `-s`：顯示簡短的主機名稱。
- `-V`：顯示版本信息。

## Common Examples
1. 顯示當前主機名稱：
   ```sh
   hostname
   ```

2. 顯示完整的主機名稱：
   ```sh
   hostname -f
   ```

3. 顯示主機的 IP 地址：
   ```sh
   hostname -i
   ```

4. 設定新的主機名稱：
   ```sh
   hostname new-hostname
   ```

5. 顯示簡短的主機名稱：
   ```sh
   hostname -s
   ```

## Tips
- 在更改主機名稱後，建議重新啟動系統以確保所有服務都能正確識別新的主機名稱。
- 使用 `hostname` 命令時，確保你有適當的權限，因為某些操作可能需要管理員權限。