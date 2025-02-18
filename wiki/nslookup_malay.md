# [Sistem Operasi] Debian Almquist Shell (dash) nslookup Penggunaan: Memeriksa alamat IP dan nama domain

## Overview
Perintah `nslookup` digunakan untuk mencari maklumat berkaitan DNS (Domain Name System). Ia membolehkan pengguna untuk mendapatkan alamat IP bagi nama domain tertentu atau sebaliknya, serta maklumat lain yang berkaitan dengan DNS.

## Usage
Sintaks asas untuk menggunakan perintah `nslookup` adalah seperti berikut:

```
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE` : Menentukan jenis rekod DNS yang ingin dicari (contohnya, A, MX, CNAME).
- `-timeout=SECONDS` : Menetapkan masa tamat untuk menunggu respons dari pelayan DNS.
- `-debug` : Mengaktifkan mod debug untuk mendapatkan maklumat lebih terperinci mengenai permintaan DNS.

## Common Examples
Berikut adalah beberapa contoh penggunaan `nslookup`:

1. **Mencari alamat IP bagi nama domain:**
   ```bash
   nslookup example.com
   ```

2. **Mencari nama domain bagi alamat IP:**
   ```bash
   nslookup 93.184.216.34
   ```

3. **Mencari rekod MX untuk domain:**
   ```bash
   nslookup -type=MX example.com
   ```

4. **Menggunakan pelayan DNS tertentu:**
   ```bash
   nslookup example.com 8.8.8.8
   ```

## Tips
- Sentiasa gunakan pelayan DNS yang dipercayai untuk mendapatkan maklumat yang tepat.
- Gunakan pilihan `-debug` jika anda menghadapi masalah untuk mendapatkan maklumat yang lebih mendalam.
- Simpan hasil pencarian yang penting untuk rujukan masa depan.