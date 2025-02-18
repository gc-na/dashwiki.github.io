# [Sistem Operasi] Debian Almquist Shell (dash) export: Menetapkan Variabel Lingkungan

## Overview
Perintah `export` digunakan untuk menetapkan variabel lingkungan dalam shell. Variabel yang diekspor dapat diakses oleh proses anak yang dijalankan dari shell saat ini, memungkinkan konfigurasi dan pengaturan yang lebih fleksibel dalam skrip dan sesi shell.

## Usage
Berikut adalah sintaks dasar dari perintah `export`:

```bash
export [options] [arguments]
```

## Common Options
- `-n`: Menghapus pengeksporan variabel, sehingga tidak lagi tersedia untuk proses anak.
- `-p`: Menampilkan semua variabel yang diekspor saat ini.
- `VAR=value`: Menetapkan nilai untuk variabel dan mengekspornya sekaligus.

## Common Examples

1. **Menetapkan dan Mengekspor Variabel Lingkungan:**
   ```bash
   export MY_VAR="Hello World"
   ```

2. **Menampilkan Variabel yang Diekspor:**
   ```bash
   export -p
   ```

3. **Menghapus Pengeksporan Variabel:**
   ```bash
   export -n MY_VAR
   ```

4. **Menetapkan dan Mengekspor Variabel dalam Satu Baris:**
   ```bash
   export PATH="$PATH:/usr/local/bin"
   ```

## Tips
- Selalu gunakan tanda kutip untuk nilai yang mengandung spasi saat mengekspor variabel.
- Gunakan `export -p` untuk memeriksa variabel yang telah diekspor sebelum menjalankan skrip.
- Pertimbangkan untuk mengekspor variabel di dalam skrip agar dapat digunakan oleh proses yang dijalankan dari skrip tersebut.