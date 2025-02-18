# [Indonesia] Debian Almquist Shell (dash) iotop: [monitor penggunaan I/O]

## Overview
Perintah `iotop` digunakan untuk memantau penggunaan I/O (Input/Output) dari proses yang berjalan di sistem. Ini membantu pengguna untuk melihat proses mana yang menggunakan sumber daya disk secara signifikan, sehingga memudahkan dalam mengidentifikasi masalah performa.

## Usage
Sintaks dasar dari perintah `iotop` adalah sebagai berikut:

```bash
iotop [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `iotop`:

- `-o`, `--only`: Menampilkan hanya proses yang sedang melakukan I/O.
- `-b`, `--batch`: Menjalankan `iotop` dalam mode batch, cocok untuk output ke file.
- `-n NUM`, `--iterations NUM`: Menentukan jumlah iterasi yang akan dijalankan sebelum keluar.
- `-d SEC`, `--delay SEC`: Menentukan waktu tunda antara pembaruan tampilan dalam detik.

## Common Examples
Berikut adalah beberapa contoh penggunaan `iotop`:

1. Menjalankan `iotop` untuk melihat semua proses yang menggunakan I/O:
   ```bash
   iotop
   ```

2. Menampilkan hanya proses yang sedang melakukan I/O:
   ```bash
   iotop -o
   ```

3. Menjalankan `iotop` dalam mode batch dan menyimpan output ke file:
   ```bash
   iotop -b -n 5 > output.txt
   ```

4. Menentukan waktu tunda antara pembaruan tampilan menjadi 2 detik:
   ```bash
   iotop -d 2
   ```

## Tips
- Gunakan opsi `-o` untuk fokus pada proses yang aktif, sehingga lebih mudah untuk mengidentifikasi masalah.
- Jalankan `iotop` dengan hak akses root untuk mendapatkan informasi yang lebih lengkap tentang semua proses.
- Pertimbangkan untuk menggunakan mode batch ketika Anda ingin merekam data untuk analisis lebih lanjut.