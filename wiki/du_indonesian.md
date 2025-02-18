# [Sistem Operasi] Debian Almquist Shell (dash) du: Menghitung penggunaan disk

## Overview
Perintah `du` (disk usage) digunakan untuk menghitung dan menampilkan penggunaan ruang disk dari file dan direktori. Ini sangat berguna untuk mengetahui seberapa banyak ruang yang digunakan oleh berbagai file dan direktori dalam sistem Anda.

## Usage
Sintaks dasar dari perintah `du` adalah sebagai berikut:

```
du [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `du`:

- `-h`: Menampilkan ukuran dalam format yang lebih mudah dibaca (misalnya, KB, MB, GB).
- `-s`: Menampilkan total penggunaan disk untuk setiap argumen, bukan untuk setiap file dan subdirektori.
- `-a`: Menampilkan penggunaan disk untuk semua file, bukan hanya direktori.
- `-c`: Menampilkan total keseluruhan penggunaan disk di akhir output.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `du`:

1. Menampilkan penggunaan disk untuk direktori saat ini:
   ```bash
   du
   ```

2. Menampilkan penggunaan disk dengan format yang lebih mudah dibaca:
   ```bash
   du -h
   ```

3. Menampilkan total penggunaan disk untuk direktori tertentu:
   ```bash
   du -sh /path/to/directory
   ```

4. Menampilkan penggunaan disk untuk semua file dan direktori dalam direktori saat ini:
   ```bash
   du -a
   ```

5. Menampilkan penggunaan disk dengan total keseluruhan di akhir:
   ```bash
   du -ch
   ```

## Tips
- Gunakan opsi `-h` untuk memudahkan pembacaan hasil, terutama jika Anda bekerja dengan file berukuran besar.
- Kombinasikan opsi `-s` dengan nama direktori untuk mendapatkan ringkasan penggunaan disk tanpa detail yang berlebihan.
- Jika Anda ingin memeriksa penggunaan disk di seluruh sistem, jalankan `du` dengan hak akses root untuk memastikan semua direktori dapat diakses.