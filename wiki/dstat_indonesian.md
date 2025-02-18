# [Sistem Operasi] Debian Almquist Shell (dash) dstat Penggunaan: Memantau sumber daya sistem secara real-time

## Overview
Perintah `dstat` adalah alat yang digunakan untuk memantau dan menampilkan statistik sumber daya sistem secara real-time. Dengan `dstat`, pengguna dapat melihat informasi tentang penggunaan CPU, memori, disk, dan jaringan dalam satu tampilan yang mudah dibaca.

## Usage
Berikut adalah sintaks dasar dari perintah `dstat`:

```bash
dstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `dstat`:

- `-c`: Menampilkan statistik penggunaan CPU.
- `-d`: Menampilkan statistik disk.
- `-n`: Menampilkan statistik jaringan.
- `-m`: Menampilkan statistik memori.
- `-t`: Menampilkan timestamp di setiap baris output.

## Common Examples
Berikut adalah beberapa contoh penggunaan `dstat`:

1. Menampilkan statistik CPU dan disk:
   ```bash
   dstat -c -d
   ```

2. Menampilkan semua statistik (CPU, disk, memori, dan jaringan):
   ```bash
   dstat -cdmn
   ```

3. Menampilkan statistik dengan timestamp:
   ```bash
   dstat -t
   ```

4. Menampilkan statistik memori dan jaringan secara bersamaan:
   ```bash
   dstat -m -n
   ```

## Tips
- Gunakan `dstat` dengan opsi `-t` untuk menambahkan timestamp, sehingga Anda dapat melacak waktu saat statistik diambil.
- Kombinasikan beberapa opsi untuk mendapatkan gambaran lengkap tentang kinerja sistem Anda.
- Jalankan `dstat` dalam terminal yang mendukung pembaruan real-time untuk melihat perubahan statistik secara langsung.