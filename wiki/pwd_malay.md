# [Sistem Operasi] Debian Almquist Shell (dash) pwd <Kegunaan>: Menunjukkan direktori kerja semasa

## Overview
Perintah `pwd` (print working directory) digunakan untuk memaparkan direktori kerja semasa dalam terminal. Ini membolehkan pengguna mengetahui lokasi mereka dalam sistem fail.

## Usage
Sintaks asas untuk perintah `pwd` adalah seperti berikut:

```
pwd [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `pwd`:

- `-L`: Menggunakan laluan simbolik semasa.
- `-P`: Menggunakan laluan fizikal, mengabaikan pautan simbolik.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `pwd`:

1. **Menunjukkan direktori kerja semasa:**
   ```bash
   pwd
   ```

2. **Menunjukkan laluan fizikal tanpa pautan simbolik:**
   ```bash
   pwd -P
   ```

3. **Menunjukkan laluan simbolik semasa:**
   ```bash
   pwd -L
   ```

## Tips
- Gunakan `pwd` sebelum menjalankan perintah lain untuk memastikan anda berada di direktori yang betul.
- Kombinasikan `pwd` dengan perintah lain seperti `cd` untuk navigasi yang lebih berkesan.
- Ingat bahawa `pwd` adalah alat yang berguna untuk pengesahan lokasi dalam skrip shell.