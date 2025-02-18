# [Sistem Operasi] Debian Almquist Shell (dash) tr <Penggunaan setara>: menukar dan memadam karakter

## Overview
Perintah `tr` dalam shell Debian Almquist (dash) digunakan untuk menukar atau memadamkan karakter dalam input. Ia sangat berguna untuk manipulasi teks, terutamanya dalam pengendalian fail atau aliran data.

## Usage
Sintaks asas untuk menggunakan perintah `tr` adalah seperti berikut:

```
tr [options] [arguments]
```

## Common Options
- `-d`: Memadamkan karakter yang ditentukan.
- `-s`: Mengurangkan urutan karakter yang berulang menjadi satu.
- `-c`: Menggunakan set karakter yang tidak ditentukan.
- `-t`: Menggantikan karakter dalam set yang ditentukan dengan karakter lain.

## Common Examples

1. **Menukar huruf kecil ke huruf besar:**
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```

2. **Memadamkan semua angka dari input:**
   ```bash
   echo "abc123def456" | tr -d '0-9'
   ```

3. **Mengurangkan urutan ruang kosong:**
   ```bash
   echo "This    is    a    test" | tr -s ' '
   ```

4. **Menukar huruf vokal ke simbol:**
   ```bash
   echo "hello" | tr 'aeiou' '*'
   ```

5. **Menggantikan karakter tertentu:**
   ```bash
   echo "apple" | tr 'ap' '12'
   ```

## Tips
- Sentiasa gunakan `echo` untuk menguji perintah `tr` sebelum menggunakannya pada fail untuk memastikan hasilnya seperti yang diharapkan.
- Anda boleh menggabungkan `tr` dengan perintah lain menggunakan paip (`|`) untuk pemprosesan yang lebih kompleks.
- Ingat bahawa `tr` hanya berfungsi pada aliran teks dan tidak dapat digunakan untuk fail binari.