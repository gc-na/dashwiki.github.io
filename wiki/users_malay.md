# [Sistem Operasi] Pengguna Debian Almquist Shell (dash): Menguruskan pengguna sistem

## Overview
Perintah `users` digunakan untuk menunjukkan nama pengguna yang sedang log masuk ke sistem pada waktu tertentu. Ia memberikan pandangan ringkas tentang pengguna aktif, yang berguna untuk pentadbir sistem dan pengguna biasa untuk memahami siapa yang sedang menggunakan sistem pada masa itu.

## Usage
Berikut adalah sintaks asas bagi perintah `users`:

```bash
users [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `users`:

- `-a`: Menunjukkan semua pengguna yang sedang log masuk, termasuk pengguna yang log masuk lebih dari sekali.
- `-n`: Menunjukkan nama pengguna tanpa menambah maklumat lain.

## Common Examples

1. **Menunjukkan pengguna yang sedang log masuk:**
   ```bash
   users
   ```

2. **Menunjukkan semua pengguna yang sedang log masuk termasuk yang log masuk lebih dari sekali:**
   ```bash
   users -a
   ```

3. **Menunjukkan nama pengguna tanpa maklumat tambahan:**
   ```bash
   users -n
   ```

## Tips
- Gunakan perintah `who` atau `w` untuk mendapatkan maklumat lebih terperinci tentang pengguna yang sedang log masuk, termasuk waktu log masuk dan aktiviti mereka.
- Perintah `users` paling berguna dalam skrip shell untuk memantau pengguna aktif secara automatik.
- Pastikan anda menjalankan perintah ini dalam terminal yang mempunyai akses kepada maklumat pengguna untuk mendapatkan hasil yang tepat.