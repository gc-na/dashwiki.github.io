# [Sistem Operasi] Debian Almquist Shell (dash) echo Penggunaan: Mencetak teks ke skrin

## Overview
Perintah `echo` dalam shell digunakan untuk mencetak teks atau output ke skrin. Ia adalah alat yang berguna untuk menampilkan mesej, nilai pembolehubah, atau hasil arahan lain.

## Usage
Sintaks asas untuk menggunakan perintah `echo` adalah seperti berikut:

```sh
echo [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `echo`:

- `-n`: Tidak mencetak karakter baru di akhir output.
- `-e`: Mengaktifkan interpretasi karakter khas seperti `\n` untuk baris baru atau `\t` untuk tab.
- `-E`: Menonaktifkan interpretasi karakter khas (ini adalah pilihan lalai).

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `echo`:

1. Mencetak teks biasa:
   ```sh
   echo "Hello, World!"
   ```

2. Mencetak tanpa baris baru di akhir:
   ```sh
   echo -n "Hello, World!"
   ```

3. Menggunakan karakter khas:
   ```sh
   echo -e "Hello,\nWorld!"
   ```

4. Mencetak nilai pembolehubah:
   ```sh
   name="John"
   echo "Hello, $name!"
   ```

5. Mencetak teks dengan tab:
   ```sh
   echo -e "Item\tPrice\nApple\t$1.00\nBanana\t$0.50"
   ```

## Tips
- Gunakan pilihan `-n` jika anda ingin mengelakkan baris baru selepas output, berguna dalam skrip.
- Pilihan `-e` membolehkan anda menggunakan karakter khas untuk format output yang lebih baik.
- Sentiasa gunakan tanda petik di sekitar teks yang mengandungi ruang untuk memastikan ia diproses dengan betul.