# [Türkçe] Debian Almquist Shell (dash) sftp Kullanımı: Dosya transferi için güvenli bir protokol

## Genel Bakış
sftp (Secure File Transfer Protocol), güvenli bir dosya transferi sağlamak için kullanılan bir protokoldür. SSH (Secure Shell) üzerinden çalışarak, dosyaların güvenli bir şekilde aktarılmasını ve yönetilmesini sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
sftp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o` : Seçenekleri belirtmek için kullanılır.
- `-b` : Bir dosyadan komutları okur.
- `-P` : Bağlantı noktası numarasını belirtir.
- `-v` : Ayrıntılı modda çalışır, hata ayıklama için kullanışlıdır.

## Yaygın Örnekler
Aşağıda sftp komutunun bazı pratik örnekleri verilmiştir:

1. **Bir sunucuya bağlanma:**
   ```bash
   sftp kullanıcı_adı@sunucu_adresi
   ```

2. **Bir dosyayı indirme:**
   ```bash
   sftp kullanıcı_adı@sunucu_adresi:/uzaktaki/dosya.txt /yerel/dosya.txt
   ```

3. **Bir dosyayı yükleme:**
   ```bash
   sftp kullanıcı_adı@sunucu_adresi
   put /yerel/dosya.txt /uzaktaki/dosya.txt
   ```

4. **Bir dizini listeleme:**
   ```bash
   sftp kullanıcı_adı@sunucu_adresi
   ls /uzaktaki/dizin
   ```

## İpuçları
- Bağlantı sırasında güvenliğinizi artırmak için anahtar tabanlı kimlik doğrulama kullanın.
- Dosya transferi yapmadan önce bağlantının güvenliğini kontrol edin.
- SFTP oturumunu kapatmayı unutmayın; `exit` veya `bye` komutları ile çıkabilirsiniz.