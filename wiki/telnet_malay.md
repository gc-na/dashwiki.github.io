# [Sistem Operasi] Debian Almquist Shell (dash) telnet: Menghubungkan ke pelayan melalui protokol Telnet

## Overview
Perintah `telnet` digunakan untuk menghubungkan ke pelayan jauh melalui protokol Telnet. Ia membolehkan pengguna untuk berinteraksi dengan pelayan secara langsung melalui baris arahan, yang sering digunakan untuk menguji sambungan rangkaian atau mengakses perkhidmatan tertentu.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `telnet`:

```
telnet [options] [arguments]
```

## Common Options
- `-l username` : Menghantar nama pengguna untuk log masuk ke pelayan.
- `-d` : Menghidupkan mod debug untuk membantu menyelesaikan masalah sambungan.
- `-n` : Menetapkan nama fail untuk log sambungan.
- `-h` : Menunjukkan bantuan dan maklumat tentang pilihan yang tersedia.

## Common Examples
Berikut adalah beberapa contoh penggunaan `telnet`:

1. **Menghubungkan ke pelayan tertentu:**
   ```bash
   telnet example.com 80
   ```

2. **Menggunakan nama pengguna untuk log masuk:**
   ```bash
   telnet -l myuser example.com
   ```

3. **Menghidupkan mod debug:**
   ```bash
   telnet -d example.com
   ```

4. **Menghubungkan ke pelayan dengan port yang berbeza:**
   ```bash
   telnet example.com 23
   ```

## Tips
- Pastikan pelayan yang ingin anda hubungi membenarkan sambungan Telnet, kerana banyak pelayan kini menggunakan protokol yang lebih selamat seperti SSH.
- Gunakan mod debug jika anda mengalami masalah sambungan untuk mendapatkan maklumat tambahan tentang apa yang mungkin salah.
- Sentiasa tutup sambungan Telnet dengan perintah `quit` untuk mengelakkan sesi terbuka yang tidak diperlukan.