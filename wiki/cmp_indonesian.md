# [Sistem Operasi] Debian Almquist Shell (dash) cmp Penggunaan: Membandingkan dua file

## Overview
Perintah `cmp` digunakan untuk membandingkan dua file byte demi byte. Jika terdapat perbedaan antara kedua file, `cmp` akan menunjukkan lokasi perbedaan tersebut. Jika file-file tersebut identik, tidak ada output yang ditampilkan.

## Usage
Berikut adalah sintaks dasar dari perintah `cmp`:

```
cmp [options] [arguments]
```

## Common Options
- `-l`: Menampilkan byte yang berbeda dalam format numerik.
- `-s`: Menyembunyikan output dan hanya mengembalikan status keluar.
- `-i OFFSET`: Mengabaikan sejumlah byte dari awal file.
- `-n N`: Membandingkan hanya N byte pertama dari kedua file.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cmp`:

1. Membandingkan dua file dan menampilkan lokasi perbedaan:
   ```bash
   cmp file1.txt file2.txt
   ```

2. Menggunakan opsi `-s` untuk hanya mendapatkan status keluar:
   ```bash
   cmp -s file1.txt file2.txt
   ```

3. Menampilkan byte yang berbeda dengan opsi `-l`:
   ```bash
   cmp -l file1.txt file2.txt
   ```

4. Mengabaikan beberapa byte dari awal file:
   ```bash
   cmp -i 10 file1.txt file2.txt
   ```

5. Membandingkan hanya N byte pertama dari kedua file:
   ```bash
   cmp -n 20 file1.txt file2.txt
   ```

## Tips
- Gunakan opsi `-s` jika Anda hanya ingin mengetahui apakah file berbeda tanpa menampilkan detail.
- Opsi `-l` sangat berguna untuk analisis mendalam ketika Anda perlu mengetahui byte mana yang berbeda.
- Pastikan untuk memeriksa status keluar dari perintah `cmp` untuk menentukan apakah file identik (status 0) atau berbeda (status 1).