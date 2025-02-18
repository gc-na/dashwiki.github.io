# [Sistem Operasi] Debian Almquist Shell (dash) wget Penggunaan: Memuat turun fail dari web

## Overview
Perintah `wget` adalah alat yang digunakan untuk memuat turun fail dari internet. Ia menyokong pelbagai protokol seperti HTTP, HTTPS, dan FTP, menjadikannya pilihan yang popular untuk mendapatkan data dari pelbagai sumber dalam talian.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `wget`:

```bash
wget [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum yang boleh digunakan dengan `wget`:

- `-q`: Mod senyap, tidak menunjukkan output.
- `-O [file]`: Menyimpan fail yang dimuat turun dengan nama yang ditentukan.
- `-c`: Melanjutkan muat turun yang terputus.
- `--limit-rate=[rate]`: Mengehadkan kelajuan muat turun.
- `-r`: Memuat turun secara rekursif, termasuk fail dalam subdirektori.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `wget`:

1. **Muat turun fail dari URL:**
   ```bash
   wget https://example.com/file.zip
   ```

2. **Menyimpan fail dengan nama tertentu:**
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. **Melanjutkan muat turun yang terputus:**
   ```bash
   wget -c https://example.com/largefile.zip
   ```

4. **Muat turun secara rekursif:**
   ```bash
   wget -r https://example.com/directory/
   ```

5. **Mengehadkan kelajuan muat turun:**
   ```bash
   wget --limit-rate=200k https://example.com/file.zip
   ```

## Tips
- Gunakan pilihan `-q` untuk mengurangkan output jika anda hanya ingin memuat turun tanpa banyak maklumat.
- Sentiasa semak URL yang anda masukkan untuk memastikan ia betul dan sah.
- Untuk muat turun yang besar, pertimbangkan menggunakan pilihan `-c` untuk mengelakkan kehilangan kemajuan jika sambungan terputus.