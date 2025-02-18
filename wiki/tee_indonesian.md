# [Sistem Operasi] Debian Almquist Shell (dash) tee Penggunaan: Menyalin dan Menampilkan Output

## Overview
Perintah `tee` digunakan untuk membaca dari input standar dan menulis ke output standar serta satu atau lebih file. Dengan kata lain, `tee` memungkinkan Anda untuk melihat output dari suatu perintah sambil juga menyimpannya ke dalam file.

## Usage
Berikut adalah sintaks dasar dari perintah `tee`:

```bash
tee [options] [arguments]
```

## Common Options
Beberapa opsi umum yang dapat digunakan dengan `tee` adalah:

- `-a`, `--append`: Menambahkan output ke file yang sudah ada, bukan menimpanya.
- `-i`, `--ignore-interrupts`: Mengabaikan sinyal interupsi.
- `-p`, `--output-error`: Mengatur perilaku ketika terjadi kesalahan saat menulis ke file.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `tee`:

1. Menyimpan output perintah ke dalam file:
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. Menyimpan output dan menampilkannya di terminal:
   ```bash
   ls -l | tee daftar_file.txt
   ```

3. Menambahkan output ke file yang sudah ada:
   ```bash
   echo "Baris baru" | tee -a output.txt
   ```

4. Menggunakan `tee` dengan beberapa file:
   ```bash
   echo "Data penting" | tee file1.txt file2.txt
   ```

## Tips
- Gunakan opsi `-a` jika Anda ingin menambahkan output ke file yang sudah ada tanpa menghapus isinya.
- Kombinasikan `tee` dengan perintah lain menggunakan pipe (`|`) untuk mengalirkan output dengan lebih efisien.
- Pastikan Anda memiliki izin yang cukup untuk menulis ke file yang dituju agar tidak mengalami kesalahan saat menggunakan `tee`.