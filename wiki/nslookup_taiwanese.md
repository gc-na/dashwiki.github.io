# [台灣] Debian Almquist Shell (dash) nslookup 使用方法: 查詢域名的IP地址

## Overview
`nslookup` 是一個用於查詢域名系統（DNS）的命令行工具。它可以幫助用戶查找特定域名的IP地址，或反向查詢IP地址以獲取相應的域名。

## Usage
基本語法如下：
```
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE`：指定查詢的記錄類型，例如 A、MX、CNAME 等。
- `-timeout=SECONDS`：設置查詢超時的時間，默認為 5 秒。
- `-retry=COUNT`：設置查詢重試的次數，默認為 4 次。

## Common Examples
查詢一個域名的IP地址：
```bash
nslookup example.com
```

查詢特定類型的DNS記錄，例如MX記錄：
```bash
nslookup -type=MX example.com
```

反向查詢IP地址以獲取域名：
```bash
nslookup 93.184.216.34
```

設置查詢的DNS伺服器：
```bash
nslookup example.com 8.8.8.8
```

## Tips
- 使用 `-type=ANY` 可以查詢所有類型的DNS記錄，但某些DNS伺服器可能不支持此選項。
- 當遇到查詢失敗時，可以嘗試更換DNS伺服器，例如使用 Google 的公共DNS（8.8.8.8）。
- 在進行大量查詢時，考慮使用 `-timeout` 和 `-retry` 來優化查詢效率。