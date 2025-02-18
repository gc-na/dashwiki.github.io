# [Türkçe] Debian Almquist Shell (dash) ping Kullanımı: Ağ bağlantısını test etme

## Genel Bakış
`ping` komutu, bir ağ üzerindeki bir hedefin erişilebilirliğini test etmek için kullanılır. Bu komut, belirli bir IP adresine veya alan adına ICMP (Internet Control Message Protocol) "echo request" paketleri gönderir ve yanıt sürelerini ölçer. Bu sayede, ağ bağlantısının durumu hakkında bilgi edinilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
ping [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c [sayı]`: Belirtilen sayıda ping gönderir ve ardından durur.
- `-i [saniye]`: Ping gönderimleri arasında bekleme süresini saniye cinsinden ayarlar.
- `-t [sayı]`: TTL (Time To Live) değerini ayarlar.
- `-s [boyut]`: Gönderilecek veri paketinin boyutunu ayarlar.

## Yaygın Örnekler
Aşağıda `ping` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Bir alan adına ping atmak:**
   ```bash
   ping www.example.com
   ```

2. **Belirli bir IP adresine ping atmak:**
   ```bash
   ping 192.168.1.1
   ```

3. **5 ping gönderip durmak:**
   ```bash
   ping -c 5 www.example.com
   ```

4. **Ping gönderimleri arasında 2 saniye beklemek:**
   ```bash
   ping -i 2 www.example.com
   ```

5. **Belirli bir paket boyutuyla ping atmak:**
   ```bash
   ping -s 100 www.example.com
   ```

## İpuçları
- Ping komutunu kullanırken, hedefin yanıt vermediği durumlarda ağ bağlantınızı kontrol edin.
- Sürekli ping atmak yerine belirli sayıda ping göndermek, ağ durumunu daha iyi analiz etmenize yardımcı olabilir.
- Ping sonuçlarını analiz ederken, kaybolan paketlerin yüzdesine dikkat edin; bu, ağda bir sorun olduğunu gösterebilir.