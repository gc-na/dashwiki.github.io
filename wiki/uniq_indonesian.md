# [Bahasa Indonesia] Debian Almquist Shell (dash) uniq Penggunaan: Menghapus baris duplikat

## Overview
Perintah `uniq` digunakan untuk menghapus baris yang duplikat dari file atau input standar. Perintah ini hanya akan menghapus baris yang berurutan, sehingga penting untuk memastikan bahwa data telah diurutkan sebelumnya jika Anda ingin menghapus semua duplikat.

## Usage
Sintaks dasar dari perintah `uniq` adalah sebagai berikut:

```
uniq [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `uniq`:

- `-c`: Menghitung jumlah kemunculan setiap baris.
- `-d`: Menampilkan hanya baris yang muncul lebih dari sekali.
- `-u`: Menampilkan hanya baris yang unik, yaitu yang muncul sekali.
- `-i`: Mengabaikan perbedaan antara huruf besar dan kecil saat membandingkan baris.

## Common Examples
Berikut adalah beberapa contoh penggunaan `uniq`:

1. Menghapus baris duplikat dari file:
   ```bash
   sort file.txt | uniq
   ```

2. Menghitung jumlah kemunculan setiap baris:
   ```bash
   sort file.txt | uniq -c
   ```

3. Menampilkan hanya baris yang muncul lebih dari sekali:
   ```bash
   sort file.txt | uniq -d
   ```

4. Menampilkan hanya baris yang unik:
   ```bash
   sort file.txt | uniq -u
   ```

5. Mengabaikan perbedaan huruf besar dan kecil:
   ```bash
   sort file.txt | uniq -i
   ```

## Tips
- Selalu gunakan `sort` sebelum `uniq` jika Anda ingin menghapus semua duplikat, karena `uniq` hanya menghapus duplikat yang berurutan.
- Gunakan opsi `-c` untuk mendapatkan gambaran tentang seberapa sering setiap baris muncul dalam data Anda.
- Jika Anda bekerja dengan file besar, pertimbangkan untuk menggunakan `uniq` dengan opsi yang sesuai untuk mengurangi output yang tidak perlu.