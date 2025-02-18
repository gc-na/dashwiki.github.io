# [Sistem Operasi] Debian Almquist Shell (dash) whoami: Menampilkan nama pengguna saat ini

## Overview
Perintah `whoami` digunakan untuk menampilkan nama pengguna yang sedang aktif di sistem. Ini berguna untuk mengetahui identitas pengguna saat ini, terutama ketika Anda bekerja dengan banyak akun atau saat menggunakan terminal.

## Usage
Berikut adalah sintaks dasar dari perintah `whoami`:

```bash
whoami [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `whoami`:

- `--help`: Menampilkan informasi bantuan tentang perintah ini.
- `--version`: Menampilkan versi dari perintah `whoami`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `whoami`:

1. Menampilkan nama pengguna saat ini:
   ```bash
   whoami
   ```

2. Menampilkan informasi bantuan:
   ```bash
   whoami --help
   ```

3. Menampilkan versi dari perintah `whoami`:
   ```bash
   whoami --version
   ```

## Tips
- Gunakan `whoami` untuk memverifikasi bahwa Anda telah masuk dengan akun yang benar sebelum menjalankan perintah yang memerlukan izin tertentu.
- Perintah ini sangat berguna dalam skrip untuk memastikan bahwa skrip dijalankan dengan pengguna yang diinginkan.