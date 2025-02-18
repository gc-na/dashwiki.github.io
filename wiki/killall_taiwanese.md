# [台灣] Debian Almquist Shell (dash) killall 使用方式: 終止所有指定進程

## Overview
`killall` 命令用於終止所有符合指定名稱的進程。這對於管理系統資源或關閉不再需要的應用程式非常有用。

## Usage
基本語法如下：
```bash
killall [選項] [進程名稱]
```

## Common Options
- `-u <用戶>`: 僅終止指定用戶所擁有的進程。
- `-q`: 安靜模式，當沒有進程被終止時不顯示錯誤訊息。
- `-I`: 忽略大小寫，終止名稱不區分大小寫的進程。

## Common Examples
- 終止所有名為 `firefox` 的進程：
```bash
killall firefox
```

- 終止所有名為 `python` 的進程，並使用安靜模式：
```bash
killall -q python
```

- 終止所有名為 `ssh` 的進程，僅限於當前用戶：
```bash
killall -u $USER ssh
```

- 終止所有名為 `java` 的進程，忽略大小寫：
```bash
killall -I java
```

## Tips
- 在使用 `killall` 前，可以使用 `pgrep` 命令確認要終止的進程名稱是否正確。
- 小心使用 `killall`，因為它會終止所有符合名稱的進程，可能會影響系統的正常運作。
- 使用 `-q` 選項可以避免在終止進程時看到不必要的錯誤訊息。