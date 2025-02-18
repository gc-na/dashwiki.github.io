# [Sistem Operasi] Debian Almquist Shell (dash) uniq Penggunaan: Menghapus baris duplikat

## Overview
Perintah `uniq` digunakan untuk menghapus baris yang berulang dalam fail teks. Ia hanya berfungsi pada baris yang bersebelahan, jadi biasanya digunakan bersama dengan perintah lain seperti `sort` untuk memastikan baris yang sama berada dalam urutan yang berdekatan.

## Usage
Berikut adalah sintaks asas untuk perintah `uniq`:

```
uniq [options] [arguments]
```

## Common Options
- `-c`: Menghitung dan menampilkan jumlah kemunculan setiap baris.
- `-d`: Menampilkan hanya baris yang muncul lebih dari sekali.
- `-u`: Menampilkan hanya baris yang unik, iaitu yang tidak berulang.
- `-i`: Mengabaikan kes (case insensitive) ketika membandingkan baris.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `uniq`:

1. **Menghapus baris duplikat dari fail:**
   ```bash
   sort fail.txt | uniq
   ```

2. **Menghitung kemunculan setiap baris:**
   ```bash
   sort fail.txt | uniq -c
   ```

3. **Menampilkan hanya baris yang berulang:**
   ```bash
   sort fail.txt | uniq -d
   ```

4. **Menampilkan hanya baris yang unik:**
   ```bash
   sort fail.txt | uniq -u
   ```

5. **Mengabaikan kes ketika membandingkan baris:**
   ```bash
   sort fail.txt | uniq -i
   ```

## Tips
- Sentiasa gunakan `sort` sebelum `uniq` untuk memastikan baris yang sama berada bersebelahan.
- Gunakan `uniq -c` untuk mendapatkan gambaran tentang berapa kali setiap baris muncul dalam fail.
- Jika anda ingin menyimpan output ke dalam fail baru, anda boleh menggunakan pengalihan output:
  ```bash
  sort fail.txt | uniq > fail_unik.txt
  ```