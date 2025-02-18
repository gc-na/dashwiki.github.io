# [Debian] Debian Almquist Shell (dash) bg: Menghantar proses ke latar belakang

## Overview
Perintah `bg` dalam shell digunakan untuk menghantar proses yang sedang berjalan ke latar belakang. Ini membolehkan pengguna meneruskan kerja lain di terminal tanpa perlu menunggu proses tersebut selesai.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `bg`:

```bash
bg [options] [arguments]
```

## Common Options
- `job_spec`: Menentukan proses tertentu yang ingin dihantar ke latar belakang. Ini biasanya ditunjukkan dengan nombor pekerjaan (job number) yang diperoleh dari perintah `jobs`.
- `-n`: Menghantar proses ke latar belakang tanpa mengeluarkan output ke terminal.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `bg`:

1. **Menghantar proses ke latar belakang**:
   Setelah menjalankan perintah yang memakan masa, anda boleh menghentikannya dengan `Ctrl + Z` dan kemudian menghantarnya ke latar belakang dengan:
   ```bash
   bg
   ```

2. **Menghantar proses tertentu ke latar belakang**:
   Jika anda mempunyai beberapa proses yang berjalan, anda boleh menghantar proses tertentu ke latar belakang dengan menyebut nombor pekerjaan:
   ```bash
   bg %1
   ```

3. **Menghantar proses ke latar belakang tanpa output**:
   Untuk menghantar proses ke latar belakang tanpa output ke terminal, gunakan:
   ```bash
   bg -n %2
   ```

## Tips
- Sentiasa semak senarai proses yang sedang berjalan dengan menggunakan perintah `jobs` sebelum menghantar proses ke latar belakang.
- Gunakan perintah `fg` untuk membawa proses yang dihantar ke latar belakang kembali ke latar depan jika perlu.
- Pastikan untuk memantau proses latar belakang anda, kerana anda mungkin kehilangan output penting jika tidak diperhatikan.