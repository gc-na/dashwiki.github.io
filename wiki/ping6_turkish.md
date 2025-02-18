# [Türkçe] Debian Almquist Shell (dash) ping6 Kullanımı: IPv6 adreslerini test etme aracı

## Genel Bakış
`ping6` komutu, bir IPv6 adresine veya hostname'e ICMPv6 Echo Request paketleri göndererek bağlantı durumunu test etmek için kullanılır. Bu komut, ağ bağlantılarının sağlıklı olup olmadığını kontrol etmek için yaygın olarak kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
ping6 [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c [sayı]`: Gönderilecek ping sayısını belirtir.
- `-i [saniye]`: Her ping arasında bekleme süresini ayarlar.
- `-s [boyut]`: Gönderilecek veri paketinin boyutunu ayarlar.
- `-W [saniye]`: Her ping yanıtı için bekleme süresini ayarlar.

## Yaygın Örnekler
Aşağıda `ping6` komutunun bazı pratik kullanımları bulunmaktadır:

1. Belirli bir IPv6 adresine ping atma:
   ```bash
   ping6 2001:db8::1
   ```

2. Belirli bir sayıda ping gönderme (örneğin 5 ping):
   ```bash
   ping6 -c 5 2001:db8::1
   ```

3. Ping gönderimleri arasında 2 saniye bekleme:
   ```bash
   ping6 -i 2 2001:db8::1
   ```

4. Özel boyutta veri paketi gönderme (örneğin 128 bayt):
   ```bash
   ping6 -s 128 2001:db8::1
   ```

## İpuçları
- Ping atarken, hedefin yanıt vermesi için yeterli süre tanıyın; çok kısa sürelerde ping atmak, ağ sorunlarını gizleyebilir.
- Ağ bağlantınızı test etmek için ping6 komutunu kullanarak, bağlantı kalitesini ve gecikmeleri gözlemleyebilirsiniz.
- Eğer ping6 komutu yanıt almıyorsa, hedef IPv6 adresinin doğru olduğundan ve ağ bağlantınızın aktif olduğundan emin olun.