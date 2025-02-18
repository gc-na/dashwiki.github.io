# [Sistem Operasi] Debian Almquist Shell (dash) grep Penggunaan: Mencari teks dalam fail

## Overview
Perintah `grep` digunakan untuk mencari teks tertentu dalam fail. Ia membolehkan pengguna menapis dan mencari baris yang mengandungi pola yang ditentukan, menjadikannya alat yang berguna untuk analisis data dan pemprosesan teks.

## Usage
Sintaks asas untuk menggunakan `grep` adalah seperti berikut:

```
grep [options] [arguments]
```

## Common Options
- `-i`: Mengabaikan kes (case insensitive).
- `-v`: Memaparkan baris yang tidak mengandungi pola yang dicari.
- `-r`: Mencari secara rekursif dalam direktori.
- `-n`: Memaparkan nombor baris bersama dengan hasil.
- `-l`: Memaparkan nama fail yang mengandungi pola yang dicari.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `grep`:

1. Mencari teks dalam fail:
   ```bash
   grep "teks" fail.txt
   ```

2. Mencari teks tanpa mengira kes:
   ```bash
   grep -i "teks" fail.txt
   ```

3. Mencari secara rekursif dalam direktori:
   ```bash
   grep -r "teks" /path/to/directory
   ```

4. Memaparkan nombor baris bersama hasil:
   ```bash
   grep -n "teks" fail.txt
   ```

5. Menunjukkan nama fail yang mengandungi pola:
   ```bash
   grep -l "teks" *.txt
   ```

## Tips
- Gunakan `grep -i` untuk mencari tanpa mengira kes, terutamanya apabila anda tidak pasti tentang huruf besar atau kecil.
- Untuk mencari lebih dari satu pola, anda boleh menggunakan `grep -E` dengan ekspresi biasa (regex).
- Simpan hasil carian ke dalam fail dengan menggunakan pengalihan output, contohnya: `grep "teks" fail.txt > hasil.txt`.