# [Sistem Operasi] Debian Almquist Shell (dash) whoami: Menunjukkan nama pengguna semasa

## Overview
Perintah `whoami` digunakan untuk menunjukkan nama pengguna yang sedang aktif dalam sesi terminal. Ini berguna untuk mengesahkan identiti pengguna yang sedang menjalankan perintah.

## Usage
Sintaks asas untuk perintah `whoami` adalah seperti berikut:

```
whoami [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `whoami`:

- `--help`: Menunjukkan maklumat bantuan tentang perintah `whoami`.
- `--version`: Menunjukkan versi perintah `whoami` yang sedang digunakan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `whoami`:

1. **Menunjukkan nama pengguna semasa:**
   ```bash
   whoami
   ```

2. **Menunjukkan maklumat bantuan:**
   ```bash
   whoami --help
   ```

3. **Menunjukkan versi perintah:**
   ```bash
   whoami --version
   ```

## Tips
- Gunakan `whoami` untuk memastikan anda sedang log masuk sebagai pengguna yang betul sebelum menjalankan perintah yang memerlukan keizinan tertentu.
- Perintah ini sangat berguna dalam skrip untuk mengesahkan identiti pengguna yang sedang menjalankan skrip tersebut.