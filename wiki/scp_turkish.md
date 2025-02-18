# [Debian] Debian Almquist Shell (dash) scp Kullanımı: Dosya transferi

## Genel Bakış
`scp` (Secure Copy Protocol), ağ üzerinden dosyaları güvenli bir şekilde kopyalamak için kullanılan bir komuttur. SSH protokolünü kullanarak, yerel ve uzak sistemler arasında dosya transferi gerçekleştirir.

## Kullanım
Temel sözdizimi şu şekildedir:
```
scp [seçenekler] [kaynak] [hedef]
```

## Yaygın Seçenekler
- `-r`: Dizini ve içindeki tüm dosyaları kopyalamak için kullanılır.
- `-P [port]`: Uzak sunucunun SSH portunu belirtmek için kullanılır (büyük P harfi ile).
- `-i [anahtar dosyası]`: Belirtilen özel anahtar dosyasını kullanarak kimlik doğrulaması yapar.
- `-v`: Ayrıntılı çıktı almak için kullanılır; hata ayıklama amacıyla faydalıdır.

## Yaygın Örnekler
Aşağıda `scp` komutunun çeşitli kullanımlarına dair örnekler bulunmaktadır:

1. Yerel bir dosyayı uzak bir sunucuya kopyalama:
   ```bash
   scp dosya.txt kullanıcı@sunucu:/hedef/klasör/
   ```

2. Uzak bir dosyayı yerel makineye indirme:
   ```bash
   scp kullanıcı@sunucu:/uzak/dosya.txt /yerel/klasör/
   ```

3. Bir dizini ve içindeki tüm dosyaları uzak bir sunucuya kopyalama:
   ```bash
   scp -r /yerel/dizin/ kullanıcı@sunucu:/hedef/dizin/
   ```

4. Belirli bir port kullanarak dosya kopyalama:
   ```bash
   scp -P 2222 dosya.txt kullanıcı@sunucu:/hedef/klasör/
   ```

## İpuçları
- Dosya transferi sırasında bağlantının kesilmesini önlemek için `-C` seçeneğini kullanarak sıkıştırma yapabilirsiniz.
- Eğer sık sık aynı sunucuya bağlanıyorsanız, SSH anahtarınızı ayarlamak, her seferinde şifre girme ihtiyacını ortadan kaldırır.
- Uzak sunucuya bağlanmadan önce bağlantı ayarlarınızı kontrol edin; doğru IP adresi ve kullanıcı adı kullandığınızdan emin olun.