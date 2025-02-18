# [Sistem Operasi] Debian Almquist Shell (dash) env: [mengurus persekitaran]

## Overview
Perintah `env` dalam dash digunakan untuk memaparkan atau mengubah suai pembolehubah persekitaran. Ia membolehkan pengguna untuk menjalankan program dalam konteks persekitaran yang berbeza dengan menetapkan pembolehubah baru atau memaparkan pembolehubah yang sedia ada.

## Usage
Sintaks asas untuk menggunakan perintah `env` adalah seperti berikut:

```
env [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `env` beserta penjelasan ringkas:

- `-i`: Mengabaikan semua pembolehubah persekitaran yang sedia ada dan memulakan dengan persekitaran kosong.
- `-u NAME`: Menghapuskan pembolehubah persekitaran yang dinamakan `NAME` sebelum menjalankan program.
- `NAME=VALUE`: Menetapkan pembolehubah persekitaran baru dengan nama `NAME` dan nilai `VALUE` sebelum menjalankan program.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `env`:

1. **Memaparkan semua pembolehubah persekitaran:**
   ```bash
   env
   ```

2. **Menjalankan program dengan pembolehubah persekitaran yang ditetapkan:**
   ```bash
   env VAR1=value1 VAR2=value2 ./my_program
   ```

3. **Mengabaikan semua pembolehubah persekitaran yang sedia ada:**
   ```bash
   env -i ./my_program
   ```

4. **Menghapuskan pembolehubah persekitaran tertentu:**
   ```bash
   env -u VAR1 ./my_program
   ```

## Tips
- Gunakan `env` untuk menguji program dalam persekitaran yang bersih dengan pilihan `-i`.
- Sentiasa semak pembolehubah persekitaran yang penting sebelum menjalankan aplikasi untuk memastikan ia berfungsi dengan betul.
- Anda boleh menggunakan `env` dalam skrip untuk menetapkan pembolehubah persekitaran yang diperlukan untuk pelbagai tugas.