# [Sistem Operasi] Debian Almquist Shell (dash) sftp Penggunaan: Memindahkan fail dengan selamat

## Overview
Perintah `sftp` (Secure File Transfer Protocol) digunakan untuk memindahkan fail dengan selamat antara komputer melalui rangkaian. Ia menyediakan sesi interaktif untuk memudahkan pemindahan fail menggunakan protokol SSH.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `sftp`:

```bash
sftp [options] [user@]hostname
```

## Common Options
- `-P port`: Menentukan nombor port untuk sambungan.
- `-o option`: Menghantar pilihan tambahan ke klien SSH.
- `-b batchfile`: Menggunakan fail batch untuk menjalankan arahan secara automatik.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sftp`:

1. **Sambung ke pelayan SFTP:**

   ```bash
   sftp user@hostname
   ```

2. **Muat naik fail ke pelayan:**

   ```bash
   sftp user@hostname
   put localfile.txt
   ```

3. **Muat turun fail dari pelayan:**

   ```bash
   sftp user@hostname
   get remotefile.txt
   ```

4. **Senaraikan fail dalam direktori pelayan:**

   ```bash
   sftp user@hostname
   ls
   ```

5. **Muat naik seluruh direktori:**

   ```bash
   sftp -r user@hostname
   put localdirectory
   ```

## Tips
- Sentiasa gunakan sambungan yang selamat dengan `sftp` untuk melindungi data anda.
- Gunakan pilihan `-b` untuk menjalankan skrip pemindahan fail secara automatik.
- Pastikan anda mempunyai kebenaran yang betul untuk mengakses fail dan direktori di pelayan.