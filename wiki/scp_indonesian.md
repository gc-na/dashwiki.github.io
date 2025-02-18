# [Sistem Operasi] Debian Almquist Shell (dash) scp: [menyalin file secara aman]

## Overview
Perintah `scp` (secure copy) digunakan untuk menyalin file atau direktori antara komputer secara aman menggunakan protokol SSH. Dengan `scp`, Anda dapat mentransfer file dengan mudah antara host lokal dan remote.

## Usage
Berikut adalah sintaks dasar dari perintah `scp`:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: Menyalin direktori secara rekursif.
- `-P port`: Menentukan port SSH yang digunakan (perhatikan huruf besar 'P').
- `-i identity_file`: Menggunakan file identitas tertentu untuk otentikasi.
- `-v`: Menampilkan informasi verbose selama proses transfer.

## Common Examples
Berikut adalah beberapa contoh penggunaan `scp`:

1. Menyalin file dari lokal ke remote:
   ```bash
   scp file.txt user@remote_host:/path/to/destination/
   ```

2. Menyalin file dari remote ke lokal:
   ```bash
   scp user@remote_host:/path/to/file.txt /local/path/
   ```

3. Menyalin direktori secara rekursif:
   ```bash
   scp -r /local/directory user@remote_host:/path/to/destination/
   ```

4. Menyalin file menggunakan port yang berbeda:
   ```bash
   scp -P 2222 file.txt user@remote_host:/path/to/destination/
   ```

## Tips
- Selalu pastikan Anda memiliki izin yang tepat untuk mengakses file dan direktori yang akan disalin.
- Gunakan opsi `-v` untuk mendapatkan informasi lebih lanjut jika terjadi kesalahan selama proses transfer.
- Jika Anda sering menggunakan `scp`, pertimbangkan untuk mengonfigurasi SSH key untuk menghindari memasukkan kata sandi setiap kali.