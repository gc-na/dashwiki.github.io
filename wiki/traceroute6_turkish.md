# [Türkçe] Debian Almquist Shell (dash) traceroute6 Kullanımı: Ağ yolunu izleme aracı

## Genel Bakış
`traceroute6` komutu, bir IPv6 adresine giden yol boyunca her bir ağ geçidini (router) izlemek için kullanılır. Bu, ağ bağlantı sorunlarını teşhis etmek ve ağın nasıl yapılandığını anlamak için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
traceroute6 [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-m <sayı>`: İzlenecek maksimum atlama sayısını belirler.
- `-p <port>`: Hedefe gönderilecek UDP paketinin port numarasını ayarlar.
- `-w <saniye>`: Her bir atlama için bekleme süresini saniye cinsinden ayarlar.

## Yaygın Örnekler
Aşağıda `traceroute6` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir IPv6 adresine giden yolu izlemek:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Maksimum 15 atlama ile bir IPv6 adresine giden yolu izlemek:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. Belirli bir port numarası ile bir IPv6 adresine giden yolu izlemek:
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. Her bir atlama için 2 saniye bekleyerek bir IPv6 adresine giden yolu izlemek:
   ```bash
   traceroute6 -w 2 2001:db8::1
   ```

## İpuçları
- `traceroute6` komutunu çalıştırmadan önce, hedef IPv6 adresinin doğru olduğundan emin olun.
- Ağ sorunlarını teşhis etmek için, farklı seçenekleri deneyerek daha fazla bilgi edinebilirsiniz.
- Ağ geçitleri hakkında daha fazla bilgi almak için, `-m` seçeneği ile atlama sayısını artırabilirsiniz.