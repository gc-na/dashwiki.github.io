# [Sistem Operasi] Debian Almquist Shell (dash) df Penggunaan: Menunjukkan penggunaan ruang disk

## Overview
Perintah `df` digunakan untuk menunjukkan penggunaan ruang disk pada sistem fail. Ia memberikan maklumat tentang jumlah ruang yang digunakan dan yang tersedia pada sistem fail yang dipasang.

## Usage
Sintaks asas untuk perintah `df` adalah seperti berikut:

```bash
df [options] [arguments]
```

## Common Options
- `-h`: Menunjukkan saiz dalam format yang mudah dibaca (seperti KB, MB, GB).
- `-T`: Menunjukkan jenis sistem fail untuk setiap sistem fail yang dipasang.
- `-a`: Menunjukkan semua sistem fail, termasuk yang tidak digunakan.
- `-i`: Menunjukkan penggunaan inode, bukan penggunaan ruang disk.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `df`:

1. Menunjukkan penggunaan ruang disk dalam format yang mudah dibaca:
   ```bash
   df -h
   ```

2. Menunjukkan jenis sistem fail untuk setiap sistem fail yang dipasang:
   ```bash
   df -T
   ```

3. Menunjukkan semua sistem fail, termasuk yang tidak digunakan:
   ```bash
   df -a
   ```

4. Menunjukkan penggunaan inode:
   ```bash
   df -i
   ```

## Tips
- Gunakan pilihan `-h` untuk memudahkan pembacaan data, terutamanya jika anda bekerja dengan sistem fail yang besar.
- Periksa penggunaan ruang disk secara berkala untuk memastikan anda tidak kehabisan ruang.
- Gabungkan pilihan seperti `-h` dan `-T` untuk mendapatkan maklumat yang lebih komprehensif dalam satu arahan.