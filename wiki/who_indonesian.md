# [Sistem Operasi] Debian Almquist Shell (dash) who: Menampilkan pengguna yang sedang masuk

## Overview
Perintah `who` digunakan untuk menampilkan daftar pengguna yang saat ini sedang masuk ke sistem. Informasi yang ditampilkan mencakup nama pengguna, terminal yang digunakan, waktu login, dan alamat IP atau hostname dari mana pengguna terhubung.

## Usage
Berikut adalah sintaks dasar dari perintah `who`:

```bash
who [options] [arguments]
```

## Common Options
- `-a`: Menampilkan semua informasi yang tersedia, termasuk pengguna yang tidak aktif.
- `-b`: Menampilkan waktu terakhir sistem di-boot.
- `-q`: Menampilkan hanya nama pengguna yang sedang masuk dan jumlah pengguna yang terhubung.
- `--help`: Menampilkan bantuan penggunaan perintah `who`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `who`:

1. Menampilkan daftar pengguna yang sedang masuk:
   ```bash
   who
   ```

2. Menampilkan semua informasi pengguna, termasuk yang tidak aktif:
   ```bash
   who -a
   ```

3. Menampilkan waktu terakhir sistem di-boot:
   ```bash
   who -b
   ```

4. Menampilkan hanya nama pengguna yang sedang masuk dan jumlah pengguna:
   ```bash
   who -q
   ```

## Tips
- Gunakan `who` secara berkala untuk memantau siapa saja yang sedang menggunakan sistem Anda.
- Kombinasikan perintah `who` dengan perintah lain seperti `grep` untuk mencari pengguna tertentu.
- Perhatikan bahwa informasi yang ditampilkan oleh `who` dapat berbeda tergantung pada konfigurasi sistem dan hak akses pengguna.