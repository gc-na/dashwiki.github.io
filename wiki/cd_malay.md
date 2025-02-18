# [Sistem Operasi] Debian Almquist Shell (dash) cd: [menukar direktori kerja]

## Overview
Perintah `cd` (change directory) digunakan dalam shell untuk menukar direktori kerja semasa. Dengan menggunakan `cd`, pengguna boleh bergerak antara pelbagai direktori dalam sistem fail.

## Usage
Sintaks asas untuk perintah `cd` adalah seperti berikut:

```bash
cd [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `cd`:

- `..` : Menukar ke direktori induk (parent directory).
- `-` : Menukar ke direktori sebelumnya.
- `~` : Menukar ke direktori home pengguna semasa.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `cd`:

1. Menukar ke direktori induk:
   ```bash
   cd ..
   ```

2. Menukar ke direktori sebelumnya:
   ```bash
   cd -
   ```

3. Menukar ke direktori home pengguna:
   ```bash
   cd ~
   ```

4. Menukar ke direktori tertentu:
   ```bash
   cd /path/to/directory
   ```

## Tips
- Gunakan `cd -` untuk kembali ke direktori sebelumnya dengan cepat.
- Untuk melihat direktori semasa, gunakan perintah `pwd` selepas menukar direktori.
- Sentiasa gunakan jalur relatif atau mutlak untuk mengelakkan kekeliruan dalam navigasi direktori.