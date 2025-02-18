# [Sistem Operasi] Debian Almquist Shell (dash) wget Penggunaan: Mengunduh file dari internet

## Overview
Perintah `wget` adalah alat yang digunakan untuk mengunduh file dari internet. Dengan `wget`, pengguna dapat mengambil file dari server web menggunakan protokol HTTP, HTTPS, dan FTP. Perintah ini sangat berguna untuk mengunduh file besar atau banyak file sekaligus.

## Usage
Berikut adalah sintaks dasar dari perintah `wget`:

```
wget [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `wget`:

- `-O <file>`: Menentukan nama file output yang diinginkan.
- `-c`: Melanjutkan unduhan yang terputus.
- `-q`: Menjalankan wget dalam mode diam (quiet), tanpa output ke layar.
- `--limit-rate=<rate>`: Membatasi kecepatan unduhan.
- `-r`: Mengunduh secara rekursif, berguna untuk mengunduh seluruh situs web.

## Common Examples
Berikut adalah beberapa contoh penggunaan `wget`:

1. Mengunduh file tunggal:
   ```bash
   wget https://example.com/file.zip
   ```

2. Mengunduh file dengan nama output yang berbeda:
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. Melanjutkan unduhan yang terputus:
   ```bash
   wget -c https://example.com/largefile.zip
   ```

4. Mengunduh seluruh situs web secara rekursif:
   ```bash
   wget -r https://example.com
   ```

5. Mengunduh file dengan batas kecepatan:
   ```bash
   wget --limit-rate=200k https://example.com/file.zip
   ```

## Tips
- Selalu periksa URL yang Anda gunakan untuk memastikan bahwa file yang diunduh adalah yang Anda inginkan.
- Gunakan opsi `-q` jika Anda ingin menjalankan unduhan di latar belakang tanpa banyak output.
- Jika mengunduh banyak file, pertimbangkan untuk menggunakan opsi `-r` untuk menghemat waktu.
- Pastikan untuk mematuhi kebijakan penggunaan bandwidth dari situs web yang Anda unduh.