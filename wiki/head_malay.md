# [Debian] Debian Almquist Shell (dash) head penggunaan: menampilkan baris awal fail

## Overview
Perintah `head` digunakan untuk memaparkan beberapa baris pertama dari fail. Ia sangat berguna untuk melihat kandungan awal fail teks tanpa perlu membuka keseluruhan fail tersebut.

## Usage
Berikut adalah sintaks asas untuk perintah `head`:

```
head [options] [arguments]
```

## Common Options
- `-n NUM`: Menentukan jumlah baris yang ingin dipaparkan. Contohnya, `-n 5` akan memaparkan 5 baris pertama.
- `-c NUM`: Menentukan jumlah bait (bytes) yang ingin dipaparkan.
- `-q`: Tidak memaparkan nama fail ketika memaparkan kandungan fail.
- `-v`: Sentiasa memaparkan nama fail walaupun hanya ada satu fail.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `head`:

1. Memaparkan 10 baris pertama dari fail `data.txt`:
   ```bash
   head data.txt
   ```

2. Memaparkan 5 baris pertama dari fail `log.txt`:
   ```bash
   head -n 5 log.txt
   ```

3. Memaparkan 20 bait pertama dari fail `file.txt`:
   ```bash
   head -c 20 file.txt
   ```

4. Memaparkan baris pertama dari beberapa fail:
   ```bash
   head file1.txt file2.txt
   ```

## Tips
- Gunakan `head` bersama dengan perintah lain melalui paip (`|`) untuk memaparkan baris awal output. Contohnya:
  ```bash
  ls -l | head -n 10
  ```
- Jika anda ingin melihat lebih banyak baris, hanya ubah nilai pada pilihan `-n`.
- Untuk fail yang sangat besar, `head` adalah cara yang cepat untuk mendapatkan gambaran awal tentang isi fail tersebut.