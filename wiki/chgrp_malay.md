# [Sistem Operasi] Debian Almquist Shell (dash) chgrp: Mengubah kumpulan pemilik fail

## Overview
Perintah `chgrp` digunakan untuk mengubah kumpulan pemilik bagi satu atau lebih fail atau direktori. Dengan menggunakan perintah ini, pengguna dapat memberikan hak akses yang sesuai kepada kumpulan tertentu.

## Usage
Berikut adalah sintaks asas untuk perintah `chgrp`:

```bash
chgrp [options] [arguments]
```

## Common Options
- `-R`: Mengubah kumpulan secara rekursif untuk semua fail dan subdirektori dalam direktori yang ditentukan.
- `-v`: Menunjukkan maklumat tentang fail yang telah diubah.
- `--reference=FILE`: Mengubah kumpulan fail kepada kumpulan fail yang ditetapkan sebagai rujukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `chgrp`:

1. Mengubah kumpulan fail tunggal:
   ```bash
   chgrp pengguna_fail myfile.txt
   ```

2. Mengubah kumpulan secara rekursif dalam direktori:
   ```bash
   chgrp -R pengguna_fail mydirectory/
   ```

3. Menggunakan fail lain sebagai rujukan:
   ```bash
   chgrp --reference=referensi.txt myfile.txt
   ```

4. Menunjukkan maklumat tentang perubahan yang dilakukan:
   ```bash
   chgrp -v pengguna_fail myfile.txt
   ```

## Tips
- Pastikan anda mempunyai hak akses yang mencukupi untuk mengubah kumpulan fail.
- Gunakan pilihan `-R` dengan berhati-hati, kerana ia akan mengubah semua fail dalam direktori yang ditentukan.
- Sentiasa semak kumpulan yang ada sebelum mengubahnya untuk mengelakkan kesilapan.