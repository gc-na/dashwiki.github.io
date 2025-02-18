# [Sistem Operasi] Debian Almquist Shell (dash) umask: [menguruskan hak akses fail]

## Overview
Perintah `umask` digunakan untuk menetapkan nilai default untuk hak akses fail yang baru dibuat. Ia menentukan jenis akses yang akan ditolak kepada pengguna, kumpulan, dan orang lain untuk fail dan direktori yang baru dicipta.

## Usage
Berikut adalah sintaks asas untuk perintah `umask`:

```bash
umask [options] [arguments]
```

## Common Options
- `-S` : Menunjukkan nilai umask dalam format simbolik.
- `-p` : Menunjukkan nilai umask semasa untuk shell yang sedang berjalan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `umask`:

1. **Menunjukkan nilai umask semasa:**

   ```bash
   umask
   ```

2. **Menetapkan umask kepada 022:**

   ```bash
   umask 022
   ```

3. **Menetapkan umask kepada 077 untuk menghalang akses kepada pengguna lain:**

   ```bash
   umask 077
   ```

4. **Menunjukkan nilai umask dalam format simbolik:**

   ```bash
   umask -S
   ```

5. **Menetapkan umask kepada 002 untuk membenarkan akses kepada kumpulan:**

   ```bash
   umask 002
   ```

## Tips
- Sentiasa semak nilai umask semasa sebelum mencipta fail penting untuk memastikan hak akses yang sesuai.
- Gunakan umask yang lebih ketat (seperti 077) untuk fail sensitif bagi meningkatkan keselamatan.
- Anda boleh menetapkan nilai umask dalam fail konfigurasi shell anda (seperti `.bashrc` atau `.profile`) untuk memastikan tetapan tersebut digunakan setiap kali anda membuka terminal.