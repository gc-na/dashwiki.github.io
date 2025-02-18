# [Bahasa Indonesia] Debian Almquist Shell (dash) comm: Membandingkan dua file baris

## Overview
Perintah `comm` digunakan untuk membandingkan dua file yang sudah diurutkan dan menampilkan baris yang unik untuk masing-masing file serta baris yang sama di antara keduanya. Ini sangat berguna untuk analisis teks dan pengolahan data.

## Usage
Berikut adalah sintaks dasar dari perintah `comm`:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Menghilangkan kolom pertama (baris unik dari file1).
- `-2`: Menghilangkan kolom kedua (baris unik dari file2).
- `-3`: Menghilangkan kolom ketiga (baris yang sama di kedua file).
- `-i`: Mengabaikan perbedaan antara huruf besar dan kecil saat membandingkan.

## Common Examples
1. **Membandingkan dua file**:
   ```bash
   comm file1.txt file2.txt
   ```

2. **Hanya menampilkan baris yang unik dari file1**:
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. **Menampilkan baris yang sama antara dua file**:
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. **Mengabaikan perbedaan huruf besar dan kecil**:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- Pastikan kedua file yang akan dibandingkan sudah diurutkan. Jika tidak, hasilnya mungkin tidak akurat.
- Gunakan opsi `-1`, `-2`, dan `-3` secara bersamaan untuk mengontrol output sesuai kebutuhan analisis Anda.
- Untuk membandingkan lebih dari dua file, pertimbangkan untuk menggunakan perintah lain seperti `diff` atau `sort` terlebih dahulu.