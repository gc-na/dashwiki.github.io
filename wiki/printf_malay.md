# [Sistem Operasi] Debian Almquist Shell (dash) printf Penggunaan: Menampilkan format teks

## Overview
Perintah `printf` dalam shell Debian Almquist (dash) digunakan untuk mencetak output ke konsol dengan format yang ditentukan. Ia membolehkan pengguna untuk mengawal cara data dipaparkan, termasuk pengisian, lebar, dan jenis data.

## Usage
Berikut adalah sintaks asas untuk perintah `printf`:

```sh
printf [options] [arguments]
```

## Common Options
- `-v var`: Menyimpan output ke dalam pembolehubah yang ditentukan.
- `--help`: Menunjukkan bantuan untuk perintah `printf`.
- `--version`: Menunjukkan versi perintah `printf`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `printf`:

1. **Mencetak teks biasa:**
   ```sh
   printf "Hello, World!\n"
   ```

2. **Mencetak dengan format integer:**
   ```sh
   printf "Nilai: %d\n" 42
   ```

3. **Mencetak dengan format floating-point:**
   ```sh
   printf "Hasil: %.2f\n" 3.14159
   ```

4. **Mencetak pelbagai argumen:**
   ```sh
   printf "Nama: %s, Umur: %d\n" "Ali" 30
   ```

5. **Menggunakan pembolehubah:**
   ```sh
   name="Siti"
   age=25
   printf "Nama: %s, Umur: %d\n" "$name" "$age"
   ```

## Tips
- Gunakan `\n` untuk menambah baris baru dalam output.
- Untuk mencetak tanda `%`, gunakan `%%` dalam format string.
- Sentiasa periksa jenis data yang ingin dicetak untuk memastikan format yang betul digunakan.