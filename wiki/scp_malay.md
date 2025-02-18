# [Sistem Operasi] Debian Almquist Shell (dash) scp: [salin fail secara selamat]

## Overview
Perintah `scp` (secure copy) digunakan untuk menyalin fail atau direktori antara komputer secara selamat menggunakan protokol SSH. Ia membolehkan pengguna untuk memindahkan fail dengan mudah dan selamat antara sistem tempatan dan jauh.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `scp`:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: Menyalin direktori secara rekursif.
- `-P`: Menentukan port SSH yang digunakan (huruf besar P).
- `-i`: Menentukan fail kunci identiti untuk pengesahan.
- `-v`: Mengaktifkan mod verbose untuk maklumat lebih lanjut tentang proses pemindahan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `scp`:

1. Menyalin fail dari sistem tempatan ke pelayan jauh:
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. Menyalin fail dari pelayan jauh ke sistem tempatan:
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. Menyalin direktori secara rekursif dari sistem tempatan ke pelayan jauh:
   ```bash
   scp -r /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
   ```

4. Menyalin fail menggunakan port SSH yang berbeza:
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tips
- Sentiasa gunakan kunci SSH untuk pengesahan yang lebih selamat berbanding kata laluan.
- Gunakan pilihan `-v` untuk menyelesaikan masalah jika pemindahan gagal.
- Pastikan anda mempunyai kebenaran yang betul untuk menyalin fail ke lokasi yang dituju.