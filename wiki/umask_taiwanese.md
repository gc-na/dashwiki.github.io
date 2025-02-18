# [台灣] Debian Almquist Shell (dash) umask 使用方式: 設定檔案權限的預設值

## Overview
`umask` 命令用來設定新檔案和目錄的預設權限。它定義了在創建新檔案或目錄時，系統會自動隱藏的權限位元。

## Usage
基本語法如下：
```sh
umask [options] [arguments]
```

## Common Options
- `-S`：以符號方式顯示當前的 umask 設定。
- `-p`：顯示當前的 umask 設定，並且不改變它。

## Common Examples
1. **查看當前 umask 設定**
   ```sh
   umask
   ```

2. **以符號方式顯示 umask 設定**
   ```sh
   umask -S
   ```

3. **設定 umask 值為 027**
   ```sh
   umask 027
   ```

4. **設定 umask 值為 002**
   ```sh
   umask 002
   ```

5. **設定 umask 值並創建新目錄**
   ```sh
   umask 007
   mkdir new_directory
   ```

## Tips
- 在設定 umask 時，請注意它是以八進位制表示，確保理解每個位元的意義。
- 常見的 umask 值有 022（對於檔案，擁有者可讀寫，其他人可讀）和 027（對於檔案，擁有者可讀寫，群組可讀）。
- 在腳本中使用 umask 可以確保檔案的權限符合安全要求。