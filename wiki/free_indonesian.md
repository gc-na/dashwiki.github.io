# [Sistem Operasi] Debian Almquist Shell (dash) free: Menampilkan informasi penggunaan memori

## Overview
Perintah `free` digunakan untuk menampilkan informasi tentang penggunaan memori dalam sistem. Ini memberikan gambaran tentang total memori, memori yang digunakan, memori yang tersedia, dan informasi lainnya yang berkaitan dengan memori sistem.

## Usage
Sintaks dasar dari perintah `free` adalah sebagai berikut:

```bash
free [options]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `free`:

- `-h`: Menampilkan ukuran memori dalam format yang lebih mudah dibaca (misalnya, KB, MB, GB).
- `-m`: Menampilkan informasi memori dalam megabyte.
- `-g`: Menampilkan informasi memori dalam gigabyte.
- `-s <detik>`: Menampilkan informasi memori secara berkala setiap `<detik>` yang ditentukan.
- `-t`: Menampilkan total memori yang digunakan dan tersedia.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `free`:

1. Menampilkan informasi memori dasar:
   ```bash
   free
   ```

2. Menampilkan informasi memori dalam format yang lebih mudah dibaca:
   ```bash
   free -h
   ```

3. Menampilkan informasi memori dalam megabyte:
   ```bash
   free -m
   ```

4. Menampilkan informasi memori dalam gigabyte:
   ```bash
   free -g
   ```

5. Menampilkan informasi memori setiap 5 detik:
   ```bash
   free -s 5
   ```

6. Menampilkan total memori yang digunakan dan tersedia:
   ```bash
   free -t
   ```

## Tips
- Gunakan opsi `-h` untuk memudahkan pemahaman informasi memori, terutama jika Anda tidak terbiasa dengan satuan ukuran memori.
- Jika Anda ingin memantau penggunaan memori secara real-time, gunakan opsi `-s` dengan interval waktu yang sesuai.
- Perintah `free` sering digunakan dalam skrip untuk memantau penggunaan memori dan membantu dalam pengelolaan sumber daya sistem.