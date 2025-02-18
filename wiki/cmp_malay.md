# [Sistem Operasi] Debian Almquist Shell (dash) cmp Penggunaan: Membandingkan dua fail

## Overview
Perintah `cmp` digunakan untuk membandingkan dua fail byte demi byte. Ia akan menunjukkan lokasi di mana fail-fail tersebut berbeza dan memberikan maklumat tentang perbezaan tersebut.

## Usage
Sintaks asas untuk perintah `cmp` adalah seperti berikut:

```bash
cmp [options] [arguments]
```

## Common Options
- `-l`: Menunjukkan perbezaan dalam format octal.
- `-s`: Tidak menghasilkan output, hanya memberikan kod keluar untuk menunjukkan sama ada fail adalah sama atau tidak.
- `-i OFFSET`: Memulakan perbandingan dari OFFSET byte.
- `-n N`: Membandingkan hanya N byte pertama dari fail.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cmp`:

1. **Membandingkan dua fail:**
   ```bash
   cmp fail1.txt fail2.txt
   ```

2. **Membandingkan dua fail dan menunjukkan perbezaan dalam format octal:**
   ```bash
   cmp -l fail1.txt fail2.txt
   ```

3. **Membandingkan dua fail tanpa output, hanya kod keluar:**
   ```bash
   cmp -s fail1.txt fail2.txt
   ```

4. **Membandingkan hanya 10 byte pertama dari dua fail:**
   ```bash
   cmp -n 10 fail1.txt fail2.txt
   ```

## Tips
- Gunakan opsi `-s` jika anda hanya ingin mengetahui sama ada fail adalah sama tanpa melihat output.
- Untuk analisis yang lebih mendalam, opsi `-l` sangat berguna untuk melihat perbezaan byte demi byte.
- Pastikan anda mempunyai izin yang betul untuk mengakses fail yang ingin dibandingkan.