# [Sistem Operasi] Debian Almquist Shell (dash) diff: membandingkan file

## Overview
Perintah `diff` digunakan untuk membandingkan isi dari dua file atau lebih dan menampilkan perbedaan di antara mereka. Ini sangat berguna untuk melihat perubahan yang telah dilakukan pada file teks, seperti kode sumber atau dokumen.

## Usage
Berikut adalah sintaks dasar dari perintah `diff`:

```bash
diff [options] [file1] [file2]
```

## Common Options
- `-u`: Menampilkan perbedaan dalam format unified, yang lebih mudah dibaca.
- `-c`: Menampilkan perbedaan dalam format context, memberikan konteks di sekitar perubahan.
- `-i`: Mengabaikan perbedaan dalam huruf besar/kecil.
- `-w`: Mengabaikan semua spasi putih saat membandingkan.
- `-r`: Membandingkan direktori secara rekursif.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `diff`:

1. **Membandingkan dua file teks sederhana:**
   ```bash
   diff file1.txt file2.txt
   ```

2. **Menggunakan opsi unified untuk hasil yang lebih jelas:**
   ```bash
   diff -u file1.txt file2.txt
   ```

3. **Membandingkan dua direktori:**
   ```bash
   diff -r dir1/ dir2/
   ```

4. **Mengabaikan perbedaan huruf besar/kecil:**
   ```bash
   diff -i file1.txt file2.txt
   ```

5. **Mengabaikan spasi putih:**
   ```bash
   diff -w file1.txt file2.txt
   ```

## Tips
- Gunakan opsi `-u` untuk melihat perbedaan dengan lebih mudah, terutama saat bekerja dengan kode sumber.
- Jika Anda bekerja dengan banyak file, pertimbangkan untuk menggunakan `diff` dengan opsi `-r` untuk membandingkan seluruh direktori.
- Simpan hasil perbandingan ke dalam file dengan menggunakan redirection:
  ```bash
  diff file1.txt file2.txt > hasil_diff.txt
  ```