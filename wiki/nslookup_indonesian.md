# [Sistem Operasi] Debian Almquist Shell (dash) nslookup Penggunaan: Mencari alamat IP dari nama domain

## Overview
Perintah `nslookup` digunakan untuk mencari informasi tentang nama domain dan alamat IP. Ini adalah alat yang berguna untuk memecahkan masalah jaringan dan mengonfirmasi konfigurasi DNS.

## Usage
Sintaks dasar dari perintah `nslookup` adalah sebagai berikut:

```
nslookup [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `nslookup`:

- `-type=TYPE` : Menentukan jenis catatan DNS yang ingin dicari (misalnya, A, AAAA, MX).
- `-timeout=SECONDS` : Mengatur waktu tunggu untuk respons DNS.
- `-retry=COUNT` : Menentukan jumlah percobaan untuk mendapatkan respons.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `nslookup`:

1. Mencari alamat IP dari nama domain:
   ```
   nslookup example.com
   ```

2. Mencari catatan MX untuk domain:
   ```
   nslookup -type=MX example.com
   ```

3. Mengatur waktu tunggu menjadi 5 detik:
   ```
   nslookup -timeout=5 example.com
   ```

4. Mencari catatan AAAA (IPv6) untuk domain:
   ```
   nslookup -type=AAAA example.com
   ```

## Tips
- Gunakan `nslookup` dalam mode interaktif dengan hanya mengetik `nslookup` untuk memasuki prompt, di mana Anda dapat melakukan beberapa pencarian tanpa harus mengetik ulang perintah.
- Pastikan untuk memeriksa konfigurasi DNS Anda jika Anda tidak mendapatkan respons yang diharapkan.
- Gunakan opsi `-retry` untuk meningkatkan peluang mendapatkan respons jika server DNS tidak merespons pada percobaan pertama.