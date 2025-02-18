# [Sistem Operasi] Debian Almquist Shell (dash) sftp: Transfer file dengan aman

## Overview
Perintah `sftp` (Secure File Transfer Protocol) digunakan untuk mentransfer file secara aman antara komputer melalui jaringan. Ini adalah bagian dari paket OpenSSH dan menyediakan cara yang aman untuk mengakses dan mengelola file di server jarak jauh.

## Usage
Berikut adalah sintaks dasar dari perintah `sftp`:

```bash
sftp [options] [user@]hostname
```

## Common Options
- `-P port`: Menentukan port yang akan digunakan untuk koneksi.
- `-i identity_file`: Menggunakan file identitas tertentu untuk otentikasi.
- `-o option`: Mengatur opsi konfigurasi tambahan.
- `-v`: Menampilkan informasi debug selama koneksi.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sftp`:

1. **Koneksi ke server SFTP:**
   ```bash
   sftp user@hostname
   ```

2. **Menggunakan port tertentu:**
   ```bash
   sftp -P 2222 user@hostname
   ```

3. **Mengunggah file ke server:**
   ```bash
   sftp user@hostname
   put localfile.txt
   ```

4. **Mengunduh file dari server:**
   ```bash
   sftp user@hostname
   get remotefile.txt
   ```

5. **Mengunggah direktori secara rekursif:**
   ```bash
   sftp user@hostname
   put -r localdir
   ```

## Tips
- Selalu gunakan koneksi yang aman dengan `sftp` untuk melindungi data Anda.
- Gunakan opsi `-v` untuk mendapatkan informasi lebih lanjut jika terjadi masalah saat koneksi.
- Simpan kredensial Anda dengan aman dan hindari menggunakan kata sandi yang lemah.