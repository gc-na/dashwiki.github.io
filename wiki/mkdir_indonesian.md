# [Indonesia] Debian Almquist Shell (dash) mkdir Penggunaan: Membuat direktori baru

## Overview
Perintah `mkdir` digunakan untuk membuat direktori baru di sistem file. Dengan menggunakan perintah ini, pengguna dapat mengorganisir file mereka dengan lebih baik dengan membuat struktur folder yang sesuai.

## Usage
Berikut adalah sintaks dasar dari perintah `mkdir`:

```
mkdir [options] [arguments]
```

## Common Options
- `-p`: Membuat direktori induk secara otomatis jika belum ada.
- `-m`: Mengatur izin akses untuk direktori yang baru dibuat.
- `-v`: Menampilkan pesan yang menunjukkan direktori yang telah dibuat.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mkdir`:

1. Membuat direktori baru:
   ```bash
   mkdir direktori_baru
   ```

2. Membuat beberapa direktori sekaligus:
   ```bash
   mkdir direktori1 direktori2 direktori3
   ```

3. Membuat direktori dengan struktur induk:
   ```bash
   mkdir -p /path/to/direktori/induk/direktori_baru
   ```

4. Mengatur izin akses saat membuat direktori:
   ```bash
   mkdir -m 755 direktori_baru
   ```

5. Menampilkan pesan saat membuat direktori:
   ```bash
   mkdir -v direktori_baru
   ```

## Tips
- Gunakan opsi `-p` untuk menghindari kesalahan saat membuat direktori yang memiliki struktur hierarki.
- Selalu periksa izin akses yang diperlukan dengan opsi `-m` untuk memastikan direktori dapat diakses oleh pengguna yang tepat.
- Gunakan opsi `-v` untuk mendapatkan umpan balik visual saat menjalankan perintah, terutama saat membuat banyak direktori.