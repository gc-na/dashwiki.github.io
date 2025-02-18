# [Sistem Operasi] Debian Almquist Shell (dash) sort penggunaan: Mengatur barisan data

## Overview
Perintah `sort` digunakan untuk mengatur barisan data dalam urutan tertentu, sama ada secara menaik atau menurun. Ia sangat berguna untuk menyusun fail teks atau output dari perintah lain.

## Usage
Sintaks asas bagi perintah `sort` adalah seperti berikut:

```
sort [options] [arguments]
```

## Common Options
- `-r`: Mengatur dalam urutan menurun.
- `-n`: Mengatur berdasarkan nilai numerik.
- `-k`: Menentukan kolum yang ingin disusun.
- `-u`: Menghapuskan baris yang berulang.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `sort`:

1. **Mengatur fail teks secara menaik:**
   ```sh
   sort fail.txt
   ```

2. **Mengatur fail teks secara menurun:**
   ```sh
   sort -r fail.txt
   ```

3. **Mengatur output dari perintah lain:**
   ```sh
   ls | sort
   ```

4. **Mengatur berdasarkan nilai numerik:**
   ```sh
   sort -n nombor.txt
   ```

5. **Mengatur berdasarkan kolum tertentu:**
   ```sh
   sort -k 2 fail.txt
   ```

6. **Menghapuskan baris yang berulang:**
   ```sh
   sort -u fail.txt
   ```

## Tips
- Sentiasa semak hasil sebelum dan selepas menggunakan `sort` untuk memastikan data disusun seperti yang diinginkan.
- Gunakan `-o` untuk menyimpan hasil pengurutan ke dalam fail yang sama:
  ```sh
  sort -o fail.txt fail.txt
  ```
- Untuk fail yang besar, pertimbangkan untuk menggunakan `sort` dengan pilihan `-S` untuk menetapkan jumlah memori yang digunakan.