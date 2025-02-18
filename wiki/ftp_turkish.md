# [Türkçe] Debian Almquist Shell (dash) ftp Kullanımı: Dosya aktarımı için bir komut

## Genel Bakış
`ftp` komutu, dosyaları bir ağ üzerinden aktarım yapmak için kullanılan bir protokoldür. Bu komut, kullanıcıların dosyaları bir FTP sunucusuna yüklemesine veya oradan indirmesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
ftp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Etkileşimli moddan çıkış yapar, yani dosya aktarımında onay istemez.
- `-v`: Ayrıntılı mod, daha fazla bilgi gösterir.
- `-n`: Otomatik olarak giriş yapmaz, kullanıcı adı ve şifre girişi gerektirir.

## Yaygın Örnekler
Aşağıda `ftp` komutunun bazı pratik örnekleri bulunmaktadır:

1. FTP sunucusuna bağlanma:
   ```bash
   ftp ftp.example.com
   ```

2. Kullanıcı adı ve şifre ile giriş yapma:
   ```bash
   ftp -n ftp.example.com
   ```
   Ardından, kullanıcı adı ve şifreyi girdikten sonra `user` komutunu kullanabilirsiniz.

3. Dosya indirme:
   ```bash
   get dosya.txt
   ```

4. Dosya yükleme:
   ```bash
   put dosya.txt
   ```

5. Tüm dosyaları indirme:
   ```bash
   mget *
   ```

## İpuçları
- FTP sunucusuna bağlanmadan önce doğru sunucu adresini ve kimlik bilgilerini kontrol edin.
- Büyük dosyalar aktarırken bağlantının kesilmemesi için `-i` seçeneğini kullanarak etkileşimli moddan çıkabilirsiniz.
- Dosya aktarım işlemlerinde hata almamak için dosya adlarını doğru yazdığınızdan emin olun.