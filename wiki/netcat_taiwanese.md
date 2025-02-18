# [台灣] Debian Almquist Shell (dash) netcat 使用法: 網路連接工具

## Overview
netcat（通常簡稱為 nc）是一個功能強大的網路工具，能夠讀取和寫入網路連接，使用 TCP 或 UDP 協議。它常被用來進行網路調試、傳輸檔案或建立簡單的伺服器和客戶端連接。

## Usage
基本語法如下：
```
netcat [options] [arguments]
```

## Common Options
- `-l`：監聽模式，讓 netcat 作為伺服器運行。
- `-p`：指定要監聽的埠號。
- `-u`：使用 UDP 協議而非 TCP。
- `-v`：啟用詳細模式，顯示更多的執行資訊。
- `-w`：設定超時時間（以秒為單位）。

## Common Examples
1. **建立 TCP 伺服器**
   ```bash
   netcat -l -p 1234
   ```
   這會在埠 1234 上啟動一個伺服器，等待連接。

2. **連接到 TCP 伺服器**
   ```bash
   netcat 192.168.1.10 1234
   ```
   這會連接到 IP 為 192.168.1.10 的伺服器，並使用埠 1234。

3. **傳輸檔案**
   在伺服器端：
   ```bash
   netcat -l -p 1234 > received_file.txt
   ```
   在客戶端：
   ```bash
   netcat 192.168.1.10 1234 < file_to_send.txt
   ```
   這會將 `file_to_send.txt` 檔案傳送到伺服器，並將其儲存為 `received_file.txt`。

4. **使用 UDP 進行連接**
   ```bash
   netcat -u -l -p 1234
   ```
   這會啟動一個 UDP 伺服器，監聽埠 1234。

## Tips
- 使用 `-v` 選項可以幫助你在調試時獲得更多的資訊。
- 當使用 netcat 傳輸檔案時，確保兩端的埠號一致。
- 在公共網路上使用 netcat 時，注意安全性，避免傳輸敏感資料。