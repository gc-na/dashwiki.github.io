# [Sistem Operasi] Debian Almquist Shell (dash) tee <Menggunakan tee>: Menyalin input ke fail dan output

## Overview
Perintah `tee` dalam shell digunakan untuk membaca dari input standard dan menulis ke output standard serta ke satu atau lebih fail. Ini membolehkan pengguna untuk melihat output di terminal sambil juga menyimpannya ke dalam fail untuk rujukan di masa hadapan.

## Usage
Sintaks asas untuk perintah `tee` adalah seperti berikut:

```bash
tee [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `tee` beserta penjelasan ringkas:

- `-a` : Menambah output ke fail yang sudah ada, bukan menimpa.
- `-i` : Mengabaikan isyarat interrupt (SIGINT).
- `--help` : Menunjukkan bantuan tentang penggunaan `tee`.
- `--version` : Menunjukkan versi `tee` yang sedang digunakan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `tee`:

1. **Menulis output ke fail**:
   ```bash
   echo "Hello, World!" | tee output.txt
   ```
   Ini akan menulis "Hello, World!" ke dalam fail `output.txt` dan juga memaparkannya di terminal.

2. **Menambah output ke fail yang sudah ada**:
   ```bash
   echo "Hello again!" | tee -a output.txt
   ```
   Ini akan menambah "Hello again!" ke dalam `output.txt` tanpa menimpa kandungan yang sedia ada.

3. **Menggunakan dengan perintah lain**:
   ```bash
   ls -l | tee directory_list.txt
   ```
   Ini akan menyenaraikan fail dalam direktori semasa dan menyimpan senarai tersebut ke dalam `directory_list.txt`.

4. **Mengabaikan isyarat interrupt**:
   ```bash
   some_long_running_command | tee -i output.txt
   ```
   Ini membolehkan `some_long_running_command` berjalan tanpa terganggu oleh isyarat interrupt.

## Tips
- Gunakan pilihan `-a` apabila anda ingin menambah output ke dalam fail tanpa menghapuskan data yang sedia ada.
- Pastikan anda mempunyai kebenaran untuk menulis ke dalam fail yang dituju.
- `tee` sangat berguna dalam skrip untuk menyimpan log output sambil memaparkannya kepada pengguna.