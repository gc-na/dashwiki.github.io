# [Sistem Operasi] Debian Almquist Shell (dash) trap Penggunaan: Mengendalikan isyarat

## Overview
Perintah `trap` dalam shell digunakan untuk menangani isyarat yang diterima oleh skrip atau proses. Ia membolehkan pengguna untuk menentukan tindakan tertentu yang perlu diambil apabila isyarat tertentu diterima, seperti menghentikan proses atau membersihkan sumber sebelum keluar.

## Usage
Sintaks asas untuk perintah `trap` adalah seperti berikut:

```sh
trap [options] [arguments]
```

## Common Options
- `SIGNAL`: Nama isyarat yang ingin ditangani (contoh: `SIGINT`, `SIGTERM`).
- `COMMAND`: Perintah yang ingin dijalankan apabila isyarat diterima.
- `-`: Menetapkan tindakan untuk mengabaikan isyarat.

## Common Examples

1. **Mengabaikan isyarat SIGINT**
   ```sh
   trap '' SIGINT
   ```
   Dalam contoh ini, isyarat `SIGINT` (biasanya dihantar dengan Ctrl+C) akan diabaikan.

2. **Menjalankan perintah sebelum keluar**
   ```sh
   trap 'echo "Skrip dihentikan"; exit' SIGINT
   ```
   Skrip ini akan mencetak mesej dan keluar apabila isyarat `SIGINT` diterima.

3. **Mengendalikan isyarat SIGTERM**
   ```sh
   trap 'echo "Proses dihentikan"; cleanup' SIGTERM
   ```
   Apabila isyarat `SIGTERM` diterima, mesej akan dicetak dan fungsi `cleanup` akan dipanggil.

4. **Menggunakan multiple traps**
   ```sh
   trap 'echo "Skrip dihentikan"; exit' SIGINT SIGTERM
   ```
   Dalam contoh ini, kedua-dua isyarat `SIGINT` dan `SIGTERM` akan memicu tindakan yang sama.

## Tips
- Sentiasa gunakan `trap` untuk memastikan bahawa skrip anda dapat menangani isyarat dengan baik, terutama untuk pembersihan sumber.
- Uji skrip anda dengan menghantar isyarat yang berbeza untuk memastikan bahawa tindakan yang ditetapkan berfungsi seperti yang diharapkan.
- Gunakan `trap -l` untuk melihat senarai semua isyarat yang boleh ditangani oleh sistem anda.