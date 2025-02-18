# [Sistem Operasi] Debian Almquist Shell (dash) ss Penggunaan: Memaparkan soket rangkaian

## Overview
Perintah `ss` digunakan untuk memaparkan dan menganalisis soket rangkaian yang sedang aktif pada sistem. Ia memberikan maklumat terperinci mengenai sambungan rangkaian, termasuk soket TCP, UDP, dan lain-lain.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `ss`:

```bash
ss [options] [arguments]
```

## Common Options
- `-t`: Memaparkan soket TCP.
- `-u`: Memaparkan soket UDP.
- `-l`: Memaparkan soket yang sedang mendengar.
- `-p`: Memaparkan proses yang berkaitan dengan soket.
- `-n`: Memaparkan alamat dan nombor port dalam format numerik.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ss`:

1. **Memaparkan semua soket TCP:**
   ```bash
   ss -t
   ```

2. **Memaparkan semua soket UDP:**
   ```bash
   ss -u
   ```

3. **Memaparkan soket yang sedang mendengar:**
   ```bash
   ss -l
   ```

4. **Memaparkan semua soket dengan maklumat proses:**
   ```bash
   ss -p
   ```

5. **Memaparkan semua soket dengan alamat dan nombor port dalam format numerik:**
   ```bash
   ss -n
   ```

## Tips
- Gunakan kombinasi pilihan untuk mendapatkan maklumat yang lebih spesifik, seperti `ss -tunlp` untuk memaparkan semua soket TCP dan UDP yang sedang mendengar bersama dengan proses yang berkaitan.
- Sentiasa periksa hak akses anda, kerana beberapa maklumat mungkin memerlukan keizinan istimewa untuk dipaparkan.
- Gunakan `man ss` untuk mendapatkan maklumat lanjut dan pilihan tambahan yang tersedia.