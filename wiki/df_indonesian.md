# [Sistem Operasi] Debian Almquist Shell (dash) df Penggunaan: Menampilkan informasi penggunaan disk

## Overview
Perintah `df` digunakan untuk menampilkan informasi tentang penggunaan ruang disk pada sistem file. Ini memberikan gambaran tentang berapa banyak ruang yang tersedia dan digunakan pada setiap sistem file yang terpasang.

## Usage
Sintaks dasar dari perintah `df` adalah sebagai berikut:

```
df [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `df`:

- `-h`: Menampilkan ukuran dalam format yang lebih mudah dibaca (misalnya, KB, MB, GB).
- `-T`: Menampilkan tipe sistem file untuk setiap sistem file yang terpasang.
- `-a`: Menampilkan semua sistem file, termasuk yang dengan penggunaan 0%.
- `-i`: Menampilkan informasi tentang inode daripada penggunaan ruang disk.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `df`:

1. Menampilkan informasi penggunaan disk dalam format yang lebih mudah dibaca:
   ```bash
   df -h
   ```

2. Menampilkan tipe sistem file untuk setiap sistem file yang terpasang:
   ```bash
   df -T
   ```

3. Menampilkan semua sistem file, termasuk yang tidak terpakai:
   ```bash
   df -a
   ```

4. Menampilkan informasi inode:
   ```bash
   df -i
   ```

## Tips
- Gunakan opsi `-h` untuk memudahkan pemahaman tentang penggunaan ruang disk, terutama jika Anda bekerja dengan ukuran besar.
- Periksa penggunaan disk secara berkala untuk menghindari kehabisan ruang yang dapat mengganggu kinerja sistem.
- Jika Anda ingin memantau penggunaan disk secara real-time, pertimbangkan untuk menggabungkan `df` dengan perintah lain seperti `watch`.