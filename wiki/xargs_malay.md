# [Sistem Operasi] Debian Almquist Shell (dash) xargs Penggunaan: Mengendalikan input dari standard input ke argumen

## Overview
Perintah `xargs` digunakan untuk membina dan menjalankan perintah berdasarkan input dari standard input. Ia sangat berguna untuk memproses output dari perintah lain dan mengubahnya menjadi argumen untuk perintah yang lain.

## Usage
Sintaks asas untuk perintah `xargs` adalah seperti berikut:

```
xargs [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `xargs` beserta penjelasannya:

- `-n N` : Menghantar N argumen kepada setiap perintah yang dijalankan.
- `-d DELIM` : Menggunakan DELIM sebagai pemisah input.
- `-0` : Menganggap input sebagai null-terminated, berguna untuk memproses nama fail dengan ruang.
- `-p` : Meminta pengesahan sebelum menjalankan setiap perintah.
- `-I {}` : Menggantikan `{}` dengan input dari standard input dalam perintah.

## Common Examples

1. **Menggunakan xargs untuk menghapus fail:**
   ```bash
   find . -name "*.tmp" | xargs rm
   ```
   Perintah ini mencari semua fail dengan akhiran `.tmp` dan menghapusnya.

2. **Menghantar argumen kepada perintah:**
   ```bash
   echo "file1.txt file2.txt" | xargs -n 1 cp {} /backup/
   ```
   Ini akan menyalin `file1.txt` dan `file2.txt` ke direktori `/backup/`.

3. **Menggunakan xargs dengan pemisah khusus:**
   ```bash
   echo "file1.txt;file2.txt" | xargs -d ';' rm
   ```
   Perintah ini menghapus fail yang dipisahkan oleh tanda titik koma.

4. **Menggunakan xargs untuk menjalankan perintah dengan pengesahan:**
   ```bash
   echo "file1.txt file2.txt" | xargs -p rm
   ```
   Ini akan meminta pengesahan sebelum menghapus setiap fail.

## Tips
- Gunakan `-n 1` untuk memproses satu argumen pada satu masa jika anda ingin mengelakkan masalah dengan perintah yang tidak dapat menerima banyak argumen.
- Sentiasa gunakan `-0` bersama dengan `find` jika nama fail mungkin mengandungi ruang atau karakter khas.
- Uji perintah anda dengan `echo` sebelum menjalankannya untuk memastikan bahawa argumen yang dihantar adalah seperti yang diharapkan.