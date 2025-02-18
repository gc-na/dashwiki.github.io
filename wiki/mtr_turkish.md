# [Türkçe] Debian Almquist Shell (dash) mtr Kullanımı: Ağ bağlantılarını izlemek için bir araç

## Genel Bakış
mtr (My Traceroute), ağ bağlantılarını izlemek ve analiz etmek için kullanılan bir komuttur. Bu araç, bir hedefe giden yol boyunca her bir yönlendiricinin (router) yanıt süresini ve kaybını gösterir. mtr, hem traceroute hem de ping işlevselliğini birleştirerek kullanıcıların ağ bağlantılarını daha etkili bir şekilde değerlendirmesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
mtr [seçenekler] [hedef]
```

## Yaygın Seçenekler
- `-r`: Rapor modunda çalışır, sonuçları bir rapor olarak gösterir.
- `-c [sayı]`: Belirtilen sayıda paket gönderir ve ardından çıkış yapar.
- `-n`: IP adreslerini çözümlemeden gösterir, bu da daha hızlı sonuçlar almanızı sağlar.
- `-p`: Her bir yönlendiricinin yanıt sürelerini gösterir.

## Yaygın Örnekler
Aşağıda mtr komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Belirli bir hedefe mtr ile bağlantı testi yapmak:
   ```bash
   mtr google.com
   ```

2. Rapor modunda belirli bir hedefe bağlantı testi yapmak:
   ```bash
   mtr -r google.com
   ```

3. 10 paket göndererek bir hedefe bağlantı testi yapmak:
   ```bash
   mtr -c 10 google.com
   ```

4. IP adreslerini çözümlemeden göstererek bir hedefe bağlantı testi yapmak:
   ```bash
   mtr -n google.com
   ```

## İpuçları
- mtr'yi kök (root) kullanıcısı olarak çalıştırmak, daha fazla bilgi elde etmenizi sağlayabilir.
- Ağ sorunlarını teşhis ederken, mtr'nin sunduğu yanıt süreleri ve kayıp yüzdelerine dikkat edin.
- mtr'yi düzenli olarak kullanarak ağ performansınızı izleyebilir ve sorunları proaktif bir şekilde tespit edebilirsiniz.