# [Sistem Operasi] Debian Almquist Shell (dash) comm: [bandingkan fail]

## Overview
Perintah `comm` digunakan untuk membandingkan dua fail yang telah disusun dan menghasilkan output yang menunjukkan baris yang unik untuk setiap fail serta baris yang sama di antara kedua-duanya. Ini sangat berguna untuk menganalisis perbezaan antara dua set data.

## Usage
Sintaks asas untuk perintah `comm` adalah seperti berikut:

```
comm [options] [arguments]
```

## Common Options
- `-1`: Mengabaikan baris yang terdapat hanya dalam fail pertama.
- `-2`: Mengabaikan baris yang terdapat hanya dalam fail kedua.
- `-3`: Mengabaikan baris yang terdapat dalam kedua-dua fail.
- `-i`: Mengabaikan kes (case insensitive) semasa membandingkan.
- `-d`: Mengeluarkan baris yang sama jika terdapat dalam kedua-dua fail.

## Common Examples

1. **Membandingkan dua fail:**
   ```bash
   comm file1.txt file2.txt
   ```

2. **Mengabaikan baris dari fail pertama:**
   ```bash
   comm -1 file1.txt file2.txt
   ```

3. **Mengabaikan baris dari fail kedua:**
   ```bash
   comm -2 file1.txt file2.txt
   ```

4. **Mengabaikan kes semasa membandingkan:**
   ```bash
   comm -i file1.txt file2.txt
   ```

5. **Mengeluarkan hanya baris yang sama:**
   ```bash
   comm -d file1.txt file2.txt
   ```

## Tips
- Pastikan kedua-dua fail yang ingin dibandingkan telah disusun. Anda boleh menggunakan perintah `sort` sebelum menggunakan `comm`.
- Gunakan pilihan `-i` jika anda ingin membandingkan teks tanpa menghiraukan huruf besar atau kecil.
- Untuk analisis yang lebih mendalam, pertimbangkan untuk menggabungkan `comm` dengan perintah lain seperti `grep` atau `awk` untuk memproses output lebih lanjut.