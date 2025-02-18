# [Sistem Operasi] Debian Almquist Shell (dash) dig: [mendapatkan maklumat DNS]

## Overview
Perintah `dig` (Domain Information Groper) digunakan untuk mendapatkan maklumat DNS (Domain Name System) untuk nama domain tertentu. Ia membolehkan pengguna untuk melakukan pertanyaan DNS dan mendapatkan maklumat seperti alamat IP, rekod MX, dan banyak lagi.

## Usage
Berikut adalah sintaks asas untuk perintah `dig`:

```bash
dig [options] [arguments]
```

## Common Options
- `@server` : Menentukan pelayan DNS yang akan digunakan untuk pertanyaan.
- `-t type` : Menentukan jenis rekod DNS yang ingin dicari (contoh: A, AAAA, MX, TXT).
- `+short` : Mengembalikan output yang lebih ringkas.
- `+trace` : Mengikuti laluan pertanyaan DNS dari akar hingga ke pelayan yang mengandungi rekod.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `dig`:

1. **Mendapatkan alamat IP untuk nama domain:**
   ```bash
   dig example.com
   ```

2. **Mendapatkan rekod MX untuk domain:**
   ```bash
   dig -t MX example.com
   ```

3. **Menggunakan pelayan DNS tertentu:**
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Mendapatkan output ringkas untuk alamat IP:**
   ```bash
   dig +short example.com
   ```

5. **Mengikuti laluan pertanyaan DNS:**
   ```bash
   dig +trace example.com
   ```

## Tips
- Gunakan `+short` untuk mendapatkan maklumat dengan lebih cepat dan mudah dibaca.
- Jika anda sering menggunakan pelayan DNS tertentu, pertimbangkan untuk menambahnya dalam fail konfigurasi DNS anda.
- Untuk analisis yang lebih mendalam, gunakan pilihan `+trace` untuk melihat bagaimana pertanyaan DNS diproses.