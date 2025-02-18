# [Sistem Operasi] Debian Almquist Shell (dash) mv Penggunaan: Memindahkan atau menamakan semula fail

## Overview
Perintah `mv` dalam shell Debian Almquist (dash) digunakan untuk memindahkan atau menamakan semula fail dan direktori. Ia adalah alat yang sangat berguna untuk menguruskan fail dalam sistem fail.

## Usage
Sintaks asas untuk menggunakan perintah `mv` adalah seperti berikut:

```bash
mv [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan perintah `mv`:

- `-i`: Menunjukkan amaran sebelum menimpa fail yang sedia ada.
- `-u`: Memindahkan fail hanya jika fail sumber lebih baru daripada fail destinasi atau jika fail destinasi tidak wujud.
- `-v`: Menunjukkan maklumat tentang fail yang sedang dipindahkan.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `mv`:

1. **Memindahkan fail ke direktori lain**:
   ```bash
   mv fail.txt /home/user/dokumen/
   ```

2. **Menamakan semula fail**:
   ```bash
   mv fail_lama.txt fail_baru.txt
   ```

3. **Memindahkan dan menamakan semula fail dalam satu perintah**:
   ```bash
   mv /home/user/fail.txt /home/user/dokumen/fail_baru.txt
   ```

4. **Memindahkan fail dengan pilihan interaktif**:
   ```bash
   mv -i fail.txt /home/user/dokumen/
   ```

## Tips
- Sentiasa gunakan pilihan `-i` jika anda tidak mahu menimpa fail secara tidak sengaja.
- Periksa semula nama fail dan direktori sebelum menjalankan perintah `mv` untuk mengelakkan kehilangan data.
- Gunakan pilihan `-v` untuk mendapatkan maklumat tambahan semasa memindahkan fail, terutamanya jika anda memindahkan banyak fail sekaligus.