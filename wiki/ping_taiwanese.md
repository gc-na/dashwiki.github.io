# [台灣] Debian Almquist Shell (dash) ping 用法: 檢查網路連線

## Overview
`ping` 命令用來檢查網路連線的狀態，透過向指定的主機發送 ICMP 回音請求，並接收回應來測試網路的可達性和延遲時間。

## Usage
基本語法如下：
```
ping [options] [arguments]
```

## Common Options
- `-c <count>`: 指定發送的請求數量。
- `-i <interval>`: 設定發送請求的間隔時間（以秒為單位）。
- `-t <ttl>`: 設定存活時間（Time To Live），控制數據包的最大跳數。
- `-s <size>`: 設定發送數據包的大小（以位元組為單位）。

## Common Examples
- 基本用法，持續發送請求到指定的主機：
  ```bash
  ping example.com
  ```

- 發送 4 次請求：
  ```bash
  ping -c 4 example.com
  ```

- 每 2 秒發送一次請求：
  ```bash
  ping -i 2 example.com
  ```

- 設定數據包大小為 64 位元組：
  ```bash
  ping -s 64 example.com
  ```

## Tips
- 使用 `-c` 選項可以避免無限循環，方便測試。
- 在測試網路延遲時，注意觀察回應時間的變化，以判斷網路的穩定性。
- 若要測試本地網路，可以使用 `ping 127.0.0.1` 或 `ping localhost`。