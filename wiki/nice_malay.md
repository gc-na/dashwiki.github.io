# [Sistem Operasi] Debian Almquist Shell (dash) nice: Mengubah keutamaan proses

## Overview
Perintah `nice` dalam shell Debian Almquist (dash) digunakan untuk menjalankan proses dengan keutamaan yang berbeza. Dengan menggunakan `nice`, pengguna boleh mengawal berapa banyak sumber CPU yang diberikan kepada proses tertentu, yang berguna untuk mengelakkan satu proses daripada mengambil semua sumber sistem.

## Usage
Sintaks asas untuk perintah `nice` adalah seperti berikut:

```
nice [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `nice` beserta penjelasan ringkas:

- `-n, --adjustment=N`: Menetapkan nilai keutamaan proses. Nilai boleh positif atau negatif.
- `--help`: Menunjukkan bantuan tentang penggunaan perintah.
- `--version`: Menunjukkan versi perintah `nice`.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `nice`:

1. Menjalankan proses dengan keutamaan yang lebih rendah:
   ```bash
   nice -n 10 myscript.sh
   ```

2. Menjalankan proses dengan keutamaan yang lebih tinggi (memerlukan hak istimewa):
   ```bash
   sudo nice -n -5 myscript.sh
   ```

3. Menjalankan perintah `top` dengan keutamaan rendah:
   ```bash
   nice -n 19 top
   ```

4. Menjalankan proses dan melihat keutamaan yang ditetapkan:
   ```bash
   nice -n 15 sleep 60
   ```

## Tips
- Gunakan `nice` untuk proses yang tidak memerlukan sumber CPU yang tinggi, seperti pemprosesan latar belakang.
- Jika anda ingin menjalankan proses dengan keutamaan yang lebih tinggi, pastikan anda mempunyai hak istimewa yang diperlukan.
- Sentiasa semak keutamaan proses yang sedang berjalan menggunakan perintah `ps` untuk memastikan sistem berfungsi dengan baik.