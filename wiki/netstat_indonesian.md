# [Indonesian] Debian Almquist Shell (dash) netstat Penggunaan: Menampilkan informasi jaringan

## Overview
Perintah `netstat` digunakan untuk menampilkan informasi tentang koneksi jaringan, tabel routing, dan statistik antarmuka jaringan. Ini sangat berguna untuk mendiagnosis masalah jaringan dan memantau aktivitas jaringan di sistem.

## Usage
Sintaks dasar dari perintah `netstat` adalah sebagai berikut:
```
netstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `netstat`:

- `-a`: Menampilkan semua koneksi dan port yang mendengarkan.
- `-t`: Menampilkan koneksi TCP.
- `-u`: Menampilkan koneksi UDP.
- `-n`: Menampilkan alamat dan nomor port dalam format numerik.
- `-l`: Menampilkan hanya port yang mendengarkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `netstat`:

1. Menampilkan semua koneksi dan port yang mendengarkan:
   ```bash
   netstat -a
   ```

2. Menampilkan hanya koneksi TCP:
   ```bash
   netstat -t
   ```

3. Menampilkan koneksi UDP dalam format numerik:
   ```bash
   netstat -un
   ```

4. Menampilkan port yang mendengarkan:
   ```bash
   netstat -l
   ```

5. Menampilkan informasi lengkap dengan alamat dan port dalam format numerik:
   ```bash
   netstat -an
   ```

## Tips
- Gunakan opsi `-p` untuk menampilkan proses yang terkait dengan setiap koneksi, jika Anda memiliki izin yang cukup.
- Kombinasikan opsi untuk mendapatkan informasi yang lebih spesifik, seperti `netstat -tunlp` untuk melihat koneksi TCP dan UDP yang mendengarkan dengan informasi proses.
- Perhatikan bahwa `netstat` mungkin tidak terinstal secara default di beberapa distribusi Linux, jadi pastikan untuk memeriksa dan menginstalnya jika diperlukan.