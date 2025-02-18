# [Sistem Operasi] Debian Almquist Shell (dash) ssh penggunaan: Menghubungkan ke pelayan secara selamat

## Overview
Perintah `ssh` (Secure Shell) digunakan untuk menghubungkan ke pelayan lain secara selamat melalui rangkaian. Ia membolehkan pengguna untuk mengakses dan mengurus sistem jauh dengan cara yang selamat, menggunakan penyulitan untuk melindungi data yang dihantar.

## Usage
Sintaks asas untuk menggunakan perintah `ssh` adalah seperti berikut:

```bash
ssh [options] [user@]hostname
```

## Common Options
Berikut adalah beberapa pilihan biasa yang digunakan dengan perintah `ssh`:

- `-p PORT` : Menentukan nombor port yang akan digunakan untuk sambungan.
- `-i ID_FILE` : Menggunakan fail kunci peribadi tertentu untuk pengesahan.
- `-v` : Mengaktifkan mod verbose untuk mendapatkan maklumat lebih lanjut tentang sambungan.
- `-X` : Mengaktifkan pengalihan X11, membolehkan aplikasi grafik berjalan di pelayan jauh.

## Common Examples
Berikut adalah beberapa contoh penggunaan `ssh`:

1. **Sambung ke pelayan dengan nama pengguna dan hostname:**
   ```bash
   ssh user@hostname
   ```

2. **Sambung ke pelayan dengan nombor port yang berbeza:**
   ```bash
   ssh -p 2222 user@hostname
   ```

3. **Sambung menggunakan fail kunci peribadi:**
   ```bash
   ssh -i ~/.ssh/id_rsa user@hostname
   ```

4. **Aktifkan mod verbose untuk pemecahan masalah:**
   ```bash
   ssh -v user@hostname
   ```

5. **Sambung dengan pengalihan X11:**
   ```bash
   ssh -X user@hostname
   ```

## Tips
- Sentiasa gunakan kunci SSH untuk pengesahan yang lebih selamat berbanding kata laluan.
- Pastikan untuk mengkonfigurasi fail `~/.ssh/config` untuk menyimpan tetapan sambungan bagi pelayan yang sering digunakan.
- Gunakan `ssh-agent` untuk mengurus kunci peribadi anda dengan lebih mudah dan selamat.