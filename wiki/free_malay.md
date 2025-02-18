# [Sistem Operasi] Debian Almquist Shell (dash) free: Menunjukkan penggunaan memori

## Overview
Perintah `free` digunakan untuk memaparkan maklumat mengenai penggunaan memori dalam sistem Linux. Ia memberikan gambaran keseluruhan tentang memori fizikal dan swap, serta memori yang sedang digunakan dan yang masih tersedia.

## Usage
Sintaks asas untuk perintah `free` adalah seperti berikut:

```
free [options] [arguments]
```

## Common Options
- `-h`: Menunjukkan nilai dalam format yang lebih mudah dibaca (contohnya, dalam MB atau GB).
- `-m`: Menunjukkan penggunaan memori dalam megabait.
- `-g`: Menunjukkan penggunaan memori dalam gigabait.
- `-s <detik>`: Menetapkan interval untuk mengemas kini maklumat secara berkala.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `free`:

1. **Paparkan penggunaan memori secara ringkas:**
   ```bash
   free
   ```

2. **Paparkan penggunaan memori dalam format yang lebih mudah dibaca:**
   ```bash
   free -h
   ```

3. **Paparkan penggunaan memori dalam megabait:**
   ```bash
   free -m
   ```

4. **Paparkan penggunaan memori dalam gigabait:**
   ```bash
   free -g
   ```

5. **Kemas kini maklumat penggunaan memori setiap 5 detik:**
   ```bash
   free -s 5
   ```

## Tips
- Gunakan pilihan `-h` untuk mendapatkan maklumat yang lebih mudah dibaca, terutamanya jika anda tidak biasa dengan angka besar.
- Untuk pemantauan berterusan, pertimbangkan menggunakan pilihan `-s` bersama dengan `watch` untuk melihat perubahan dalam penggunaan memori secara langsung.
- Sentiasa periksa penggunaan memori sebelum menjalankan aplikasi berat untuk memastikan sistem anda mempunyai sumber yang mencukupi.