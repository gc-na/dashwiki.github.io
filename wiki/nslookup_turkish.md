# [Türkçe] Debian Almquist Shell (dash) nslookup Kullanımı: DNS sorgulama aracı

## Genel Bakış
`nslookup`, bir alan adının IP adresini veya bir IP adresinin alan adını sorgulamak için kullanılan bir komuttur. DNS (Domain Name System) ile etkileşimde bulunarak, kullanıcıların ağ üzerindeki kaynakları bulmasına yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
nslookup [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-type=TYPE`: Sorgulamak istediğiniz DNS kaynağının türünü belirtir (örneğin, A, MX, CNAME).
- `-timeout=NUM`: Sorgunun zaman aşımını saniye cinsinden ayarlar.
- `-retry=NUM`: Sorgu için deneme sayısını belirler.
- `-debug`: Ayrıntılı hata ayıklama bilgilerini görüntüler.

## Yaygın Örnekler
1. Bir alan adının IP adresini sorgulama:
   ```bash
   nslookup example.com
   ```

2. Belirli bir DNS kaynağı türünü sorgulama (örneğin, MX kaydı):
   ```bash
   nslookup -type=MX example.com
   ```

3. Belirli bir DNS sunucusunu kullanarak sorgulama:
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. Bir IP adresinin alan adını sorgulama:
   ```bash
   nslookup 93.184.216.34
   ```

## İpuçları
- Sorgulama yapmadan önce DNS sunucusunun doğru çalıştığından emin olun.
- Sık kullanılan DNS kayıt türlerini öğrenmek, daha etkili sorgular yapmanıza yardımcı olabilir.
- `-debug` seçeneğini kullanarak sorun giderme sırasında daha fazla bilgi edinebilirsiniz.