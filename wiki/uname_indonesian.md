# [Linux] Debian Almquist Shell (dash) uname Penggunaan: Menampilkan informasi sistem

## Overview
Perintah `uname` digunakan untuk menampilkan informasi tentang sistem operasi yang sedang berjalan. Ini termasuk nama kernel, versi, dan informasi lainnya yang relevan dengan sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `uname`:

```
uname [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `uname`:

- `-a`: Menampilkan semua informasi sistem.
- `-s`: Menampilkan nama kernel.
- `-n`: Menampilkan nama jaringan (hostname).
- `-r`: Menampilkan versi kernel.
- `-v`: Menampilkan informasi versi tambahan.
- `-m`: Menampilkan arsitektur mesin.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `uname`:

1. Menampilkan semua informasi sistem:
   ```sh
   uname -a
   ```

2. Menampilkan nama kernel:
   ```sh
   uname -s
   ```

3. Menampilkan versi kernel:
   ```sh
   uname -r
   ```

4. Menampilkan arsitektur mesin:
   ```sh
   uname -m
   ```

5. Menampilkan nama jaringan:
   ```sh
   uname -n
   ```

## Tips
- Gunakan opsi `-a` untuk mendapatkan gambaran lengkap tentang sistem Anda dalam satu perintah.
- Perintah `uname` sangat berguna dalam skrip untuk memeriksa versi kernel sebelum menjalankan perintah lain yang bergantung pada versi tersebut.
- Ingat bahwa informasi yang ditampilkan oleh `uname` dapat bervariasi tergantung pada sistem operasi dan konfigurasi kernel yang digunakan.