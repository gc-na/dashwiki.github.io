# [Sistem Operasi] Debian Almquist Shell (dash) umask: Mengatur izin file default

## Overview
Perintah `umask` digunakan untuk mengatur izin file default yang diberikan kepada file dan direktori baru yang dibuat oleh pengguna. Ini menentukan izin akses yang akan ditetapkan secara otomatis saat file atau direktori baru dibuat.

## Usage
Berikut adalah sintaks dasar dari perintah `umask`:

```bash
umask [options] [arguments]
```

## Common Options
- `-S`: Menampilkan nilai umask dalam format simbolik.
- `-p`: Menampilkan nilai umask saat ini dan tidak mengubahnya.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `umask`:

1. **Menampilkan nilai umask saat ini:**
   ```bash
   umask
   ```

2. **Mengatur umask menjadi 022:**
   ```bash
   umask 022
   ```

3. **Mengatur umask menjadi 077:**
   ```bash
   umask 077
   ```

4. **Menampilkan nilai umask dalam format simbolik:**
   ```bash
   umask -S
   ```

5. **Menampilkan nilai umask saat ini tanpa mengubahnya:**
   ```bash
   umask -p
   ```

## Tips
- Pastikan untuk memeriksa nilai umask Anda sebelum membuat file atau direktori baru untuk memastikan izin yang sesuai.
- Gunakan umask yang lebih ketat (seperti 077) jika Anda bekerja dengan informasi sensitif untuk meningkatkan keamanan.
- Anda dapat menambahkan perintah `umask` ke file konfigurasi shell Anda (seperti `.bashrc` atau `.profile`) untuk mengatur nilai default setiap kali Anda membuka terminal.