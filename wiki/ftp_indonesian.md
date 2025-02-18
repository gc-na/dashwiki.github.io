# [Sistem Operasi] Debian Almquist Shell (dash) ftp: Mengelola Transfer File

## Overview
Perintah `ftp` digunakan untuk mentransfer file antara komputer melalui protokol File Transfer Protocol (FTP). Dengan `ftp`, pengguna dapat mengunggah, mengunduh, dan mengelola file di server FTP.

## Usage
Berikut adalah sintaks dasar dari perintah `ftp`:

```
ftp [options] [arguments]
```

## Common Options
Beberapa opsi umum yang dapat digunakan dengan perintah `ftp` antara lain:

- `-i`: Menonaktifkan mode interaktif, sehingga tidak meminta konfirmasi sebelum mengirim file.
- `-n`: Menghindari login otomatis ke server FTP.
- `-v`: Menampilkan informasi lebih detail selama proses transfer.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ftp`:

1. **Menghubungkan ke server FTP:**
   ```bash
   ftp ftp.example.com
   ```

2. **Mengunggah file ke server:**
   ```bash
   ftp> put file.txt
   ```

3. **Mengunduh file dari server:**
   ```bash
   ftp> get file.txt
   ```

4. **Mengunggah beberapa file sekaligus:**
   ```bash
   ftp> mput *.txt
   ```

5. **Mengunduh beberapa file sekaligus:**
   ```bash
   ftp> mget *.jpg
   ```

## Tips
- Selalu pastikan untuk menggunakan koneksi yang aman saat mentransfer file sensitif.
- Gunakan opsi `-i` jika Anda ingin mengunggah banyak file tanpa konfirmasi.
- Jika Anda sering terhubung ke server yang sama, pertimbangkan untuk menggunakan file `.netrc` untuk menyimpan kredensial login Anda.