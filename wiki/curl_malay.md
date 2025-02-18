# [Sistem Operasi] Debian Almquist Shell (dash) curl Penggunaan: Mengambil data dari URL

## Overview
Perintah `curl` digunakan untuk memindahkan data dari atau ke pelayan menggunakan protokol yang berbeza seperti HTTP, HTTPS, FTP, dan banyak lagi. Ia sangat berguna untuk menguji API, memuat turun fail, dan berinteraksi dengan pelayan web.

## Usage
Sintaks asas untuk menggunakan `curl` adalah seperti berikut:

```bash
curl [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang digunakan dengan `curl`:

- `-o <file>`: Menyimpan output ke dalam fail yang ditentukan.
- `-O`: Menyimpan output dengan nama fail yang sama seperti di pelayan.
- `-I`: Mengambil hanya header HTTP.
- `-d <data>`: Menghantar data sebagai permintaan POST.
- `-H <header>`: Menambah header khusus pada permintaan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `curl`:

1. **Mengambil halaman web:**
   ```bash
   curl http://example.com
   ```

2. **Menyimpan output ke dalam fail:**
   ```bash
   curl -o myfile.html http://example.com
   ```

3. **Mengambil hanya header HTTP:**
   ```bash
   curl -I http://example.com
   ```

4. **Menghantar data dengan permintaan POST:**
   ```bash
   curl -d "name=John&age=30" http://example.com/api
   ```

5. **Menambah header khusus:**
   ```bash
   curl -H "Authorization: Bearer token" http://example.com/api
   ```

## Tips
- Gunakan `-v` untuk mengaktifkan mod verbose yang memberikan maklumat terperinci tentang permintaan dan respons.
- Sentiasa periksa dokumentasi rasmi `curl` untuk pilihan tambahan dan penggunaan lanjutan.
- Untuk memudahkan debugging, gunakan `--trace` untuk mendapatkan maklumat lengkap tentang permintaan yang dihantar.