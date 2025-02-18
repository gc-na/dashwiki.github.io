# [台灣] Debian Almquist Shell (dash) dig 用法: 查詢 DNS 資訊

## Overview
`dig` 是一個用於查詢 DNS（域名系統）資訊的命令行工具。它可以幫助用戶獲取有關域名的詳細資料，例如 IP 地址、MX 記錄等。

## Usage
基本語法如下：
```
dig [選項] [參數]
```

## Common Options
- `@server`：指定要查詢的 DNS 伺服器。
- `-t type`：指定查詢的記錄類型，例如 A、AAAA、MX 等。
- `+short`：僅顯示簡短的查詢結果。
- `-x`：進行反向查詢，根據 IP 地址查找域名。

## Common Examples
以下是一些常見的 `dig` 使用範例：

1. 查詢某個域名的 A 記錄：
   ```bash
   dig example.com
   ```

2. 查詢特定 DNS 伺服器的 A 記錄：
   ```bash
   dig @8.8.8.8 example.com
   ```

3. 查詢 MX 記錄：
   ```bash
   dig example.com -t MX
   ```

4. 進行反向查詢：
   ```bash
   dig -x 8.8.8.8
   ```

5. 獲取簡短的查詢結果：
   ```bash
   dig example.com +short
   ```

## Tips
- 使用 `+trace` 選項可以查看查詢的整個過程，這對於故障排除非常有幫助。
- 結合使用 `-t` 和 `+short` 可以快速獲取特定記錄的簡短結果。
- 定期檢查 DNS 記錄可以幫助確保網站的可用性和性能。