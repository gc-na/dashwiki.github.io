# [Sistem Operasi] Debian Almquist Shell (dash) nice: Mengatur prioritas proses

## Overview
Perintah `nice` digunakan untuk mengatur prioritas eksekusi proses di sistem operasi Unix-like, termasuk Debian. Dengan `nice`, pengguna dapat menentukan seberapa besar prioritas yang diberikan kepada suatu proses saat dijalankan, yang dapat membantu dalam mengelola sumber daya sistem.

## Usage
Sintaks dasar dari perintah `nice` adalah sebagai berikut:

```bash
nice [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `nice`:

- `-n, --adjustment=N`: Menentukan nilai penyesuaian prioritas, di mana N adalah angka dari -20 (prioritas tertinggi) hingga 19 (prioritas terendah).
- `-h, --help`: Menampilkan bantuan tentang penggunaan perintah `nice`.
- `--version`: Menampilkan versi dari perintah `nice`.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `nice`:

1. Menjalankan perintah `sleep` dengan prioritas default:
   ```bash
   nice sleep 10
   ```

2. Menjalankan perintah `gzip` dengan prioritas lebih rendah:
   ```bash
   nice -n 10 gzip file.txt
   ```

3. Menjalankan perintah `make` dengan prioritas lebih tinggi:
   ```bash
   nice -n -5 make
   ```

4. Menjalankan skrip `backup.sh` dengan prioritas normal:
   ```bash
   nice ./backup.sh
   ```

## Tips
- Gunakan nilai negatif untuk memberikan prioritas lebih tinggi kepada proses yang penting, sehingga mereka mendapatkan lebih banyak sumber daya CPU.
- Sebaiknya gunakan `nice` saat menjalankan proses yang memakan waktu lama, agar tidak mengganggu proses lain yang lebih penting.
- Periksa prioritas proses yang sedang berjalan dengan menggunakan perintah `ps` untuk memastikan pengaturan prioritas yang tepat.