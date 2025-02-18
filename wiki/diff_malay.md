# [Sistem Operasi] Debian Almquist Shell (dash) diff: Membandingkan fail

## Overview
Perintah `diff` digunakan untuk membandingkan dua fail teks dan menunjukkan perbezaan antara mereka. Ia sangat berguna untuk melihat perubahan yang dibuat pada fail, terutamanya dalam konteks pengaturcaraan dan pengurusan versi.

## Usage
Berikut adalah sintaks asas untuk perintah `diff`:

```bash
diff [options] [arguments]
```

## Common Options
- `-u`: Menunjukkan perbezaan dalam format unified, yang lebih mudah dibaca.
- `-c`: Menunjukkan perbezaan dalam format context, memberikan lebih banyak konteks di sekitar perubahan.
- `-i`: Mengabaikan perbezaan dalam huruf besar dan kecil.
- `-w`: Mengabaikan semua ruang kosong dalam perbandingan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `diff`:

1. **Membandingkan dua fail teks**:
   ```bash
   diff fail1.txt fail2.txt
   ```

2. **Menggunakan pilihan unified**:
   ```bash
   diff -u fail1.txt fail2.txt
   ```

3. **Mengabaikan huruf besar dan kecil**:
   ```bash
   diff -i fail1.txt fail2.txt
   ```

4. **Mengabaikan ruang kosong**:
   ```bash
   diff -w fail1.txt fail2.txt
   ```

5. **Mendapatkan perbezaan dalam format context**:
   ```bash
   diff -c fail1.txt fail2.txt
   ```

## Tips
- Sentiasa gunakan pilihan `-u` untuk mendapatkan output yang lebih mudah dibaca.
- Jika anda bekerja dengan fail yang sering berubah, pertimbangkan untuk menggunakan alat pengurusan versi seperti Git yang mengintegrasikan `diff` secara automatik.
- Simpan salinan fail asal sebelum melakukan perubahan besar, agar anda dapat membandingkan dengan mudah menggunakan `diff`.