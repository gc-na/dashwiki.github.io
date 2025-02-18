# [Sistem Operasi] Debian Almquist Shell (dash) rsync Penggunaan: Menyalin dan menyelaraskan fail

## Overview
Rsync adalah alat yang digunakan untuk menyalin dan menyelaraskan fail dan direktori antara lokasi yang berbeza. Ia sangat berguna untuk membuat salinan sandaran, menyelaraskan fail antara pelayan, dan memindahkan data dengan cekap.

## Usage
Sintaks asas untuk menggunakan rsync adalah seperti berikut:
```
rsync [options] [arguments]
```

## Common Options
- `-a`: Mengaktifkan mod arkib, yang menyalin fail dan direktori secara rekursif dan mengekalkan atribut fail.
- `-v`: Mengaktifkan mod verbose, yang memberikan maklumat lebih lanjut semasa proses pemindahan.
- `-z`: Mengaktifkan pemampatan semasa pemindahan, berguna untuk memindahkan fail besar melalui rangkaian.
- `--delete`: Menghapus fail di lokasi destinasi yang tidak ada di lokasi sumber.
- `-r`: Menyalin direktori secara rekursif.

## Common Examples
Berikut adalah beberapa contoh penggunaan rsync:

1. Menyalin fail dari satu direktori ke direktori lain:
   ```bash
   rsync -av /path/sumber/ /path/destinasi/
   ```

2. Menyalin fail ke pelayan jauh menggunakan SSH:
   ```bash
   rsync -avz /path/sumber/ pengguna@pelayan:/path/destinasi/
   ```

3. Menyelaraskan direktori dan menghapus fail yang tidak ada di sumber:
   ```bash
   rsync -av --delete /path/sumber/ /path/destinasi/
   ```

4. Menyalin fail dengan pemampatan:
   ```bash
   rsync -avz /path/sumber/ /path/destinasi/
   ```

## Tips
- Sentiasa gunakan pilihan `-n` (dry run) sebelum menjalankan rsync untuk melihat apa yang akan dilakukan tanpa membuat sebarang perubahan.
- Gunakan pilihan `-e` untuk menentukan protokol pengangkutan yang berbeza jika perlu, seperti SSH.
- Pastikan untuk menambah `/` di akhir direktori sumber jika anda ingin menyalin isi direktori, bukan direktori itu sendiri.