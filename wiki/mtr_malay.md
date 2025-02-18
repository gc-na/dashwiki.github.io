# [Sistem Operasi] Debian Almquist Shell (dash) mtr Penggunaan: Menyemak laluan rangkaian

## Overview
Perintah `mtr` (My Traceroute) adalah alat yang menggabungkan fungsi `ping` dan `traceroute` untuk mendiagnosis masalah rangkaian. Ia membolehkan pengguna melihat laluan yang diambil oleh paket data dari komputer mereka ke destinasi tertentu, serta mengukur masa perjalanan dan kehilangan paket di setiap hop.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `mtr`:

```
mtr [options] [arguments]
```

## Common Options
- `-r`: Menjalankan dalam mod laporan, hanya menunjukkan hasil pada akhir.
- `-c <count>`: Menentukan bilangan paket yang dihantar sebelum menghentikan pengukuran.
- `-i <interval>`: Menetapkan selang masa antara paket yang dihantar.
- `-p`: Menunjukkan nombor port yang digunakan untuk sambungan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mtr`:

1. Menjalankan `mtr` ke alamat IP atau nama host:
   ```bash
   mtr google.com
   ```

2. Menjalankan `mtr` dengan mod laporan:
   ```bash
   mtr -r google.com
   ```

3. Menghantar 10 paket ke alamat tertentu:
   ```bash
   mtr -c 10 google.com
   ```

4. Menetapkan selang 1 saat antara paket:
   ```bash
   mtr -i 1 google.com
   ```

## Tips
- Gunakan mod laporan (`-r`) untuk mendapatkan ringkasan yang lebih mudah dibaca.
- Jika mengalami masalah sambungan, jalankan `mtr` ke pelayan yang berbeza untuk menentukan sama ada masalahnya terletak pada rangkaian tempatan atau jauh.
- Perhatikan kehilangan paket dan masa perjalanan untuk setiap hop untuk mengenal pasti titik lemah dalam rangkaian.