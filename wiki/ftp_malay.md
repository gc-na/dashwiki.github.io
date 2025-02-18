# [Debian] Debian Almquist Shell (dash) ftp penggunaan: Mengurus pemindahan fail melalui protokol FTP

## Overview
Perintah `ftp` digunakan untuk mengurus pemindahan fail antara komputer melalui protokol File Transfer Protocol (FTP). Ia membolehkan pengguna untuk menyambung ke pelayan FTP, memuat turun atau memuat naik fail, serta menguruskan fail dan direktori di pelayan.

## Usage
Sintaks asas bagi perintah `ftp` adalah seperti berikut:

```bash
ftp [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `ftp`:

- `-i`: Mematikan mod interaktif, membolehkan pemindahan fail tanpa meminta pengesahan.
- `-n`: Menghalang ftp daripada secara automatik menyambung ke pelayan FTP.
- `-v`: Mengaktifkan mod verbose, yang memberikan maklumat tambahan tentang proses pemindahan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `ftp`:

1. **Sambung ke pelayan FTP:**
   ```bash
   ftp ftp.example.com
   ```

2. **Sambung tanpa pengesahan automatik:**
   ```bash
   ftp -n ftp.example.com
   ```

3. **Muat turun fail dari pelayan:**
   ```bash
   get filename.txt
   ```

4. **Muat naik fail ke pelayan:**
   ```bash
   put filename.txt
   ```

5. **Mendapatkan senarai fail dalam direktori:**
   ```bash
   ls
   ```

## Tips
- Sentiasa gunakan mod `-i` jika anda ingin memindahkan banyak fail secara serentak untuk mengelakkan pengesahan berulang.
- Pastikan anda mempunyai kebenaran yang betul untuk memuat naik atau memuat turun fail dari pelayan.
- Gunakan mod verbose (`-v`) untuk mendapatkan maklumat tambahan jika anda menghadapi masalah semasa pemindahan fail.