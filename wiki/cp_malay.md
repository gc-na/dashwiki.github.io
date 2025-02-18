# [Sistem Operasi] Debian Almquist Shell (dash) cp: [salin fail]

## Overview
Perintah `cp` digunakan untuk menyalin fail dan direktori dalam sistem fail. Ia membolehkan pengguna untuk membuat salinan fail yang sedia ada ke lokasi baru, sama ada dengan nama yang sama atau nama yang berbeza.

## Usage
Sintaks asas untuk perintah `cp` adalah seperti berikut:

```bash
cp [options] [source] [destination]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan perintah `cp`:

- `-r`: Menyalin direktori secara rekursif.
- `-i`: Meminta pengesahan sebelum menimpa fail yang sedia ada.
- `-u`: Menyalin hanya fail yang lebih baru daripada fail yang sedia ada di destinasi.
- `-v`: Menunjukkan fail yang sedang disalin (verbose).

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `cp`:

1. Menyalin fail ke lokasi lain:
   ```bash
   cp fail.txt /home/user/dokumen/
   ```

2. Menyalin fail dengan nama baru:
   ```bash
   cp fail.txt fail_baru.txt
   ```

3. Menyalin direktori secara rekursif:
   ```bash
   cp -r direktori_sumber/ direktori_destinasi/
   ```

4. Menyalin fail dengan pengesahan sebelum menimpa:
   ```bash
   cp -i fail_lama.txt /home/user/dokumen/
   ```

5. Menyalin hanya fail yang lebih baru:
   ```bash
   cp -u fail.txt /home/user/dokumen/
   ```

## Tips
- Sentiasa gunakan pilihan `-i` jika anda bimbang tentang menimpa fail yang sedia ada.
- Gunakan pilihan `-v` untuk mendapatkan maklumat tentang proses penyalinan, terutamanya apabila menyalin banyak fail.
- Pastikan anda mempunyai izin yang mencukupi untuk menyalin fail ke lokasi destinasi.