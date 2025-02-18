# [Türkçe] Debian Almquist Shell (dash) traceroute Kullanımı: Ağ yolunu izleme aracı

## Genel Bakış
`traceroute` komutu, bir ağ üzerindeki bir hedefe ulaşmak için geçen yönlendiricilerin (router) listesini gösterir. Bu, ağ bağlantı sorunlarını teşhis etmek ve ağın yapısını anlamak için yararlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
traceroute [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-m <sayı>`: Maksimum sıçrama sayısını belirler.
- `-n`: IP adreslerini çözümlemeden, yalnızca sayısal IP adreslerini gösterir.
- `-p <port>`: Hedefe ulaşmak için kullanılacak port numarasını belirtir.
- `-w <saniye>`: Her bir sıçrama için bekleme süresini ayarlar.

## Yaygın Örnekler
Aşağıda `traceroute` komutunun bazı pratik örnekleri bulunmaktadır:

1. Basit bir traceroute:
    ```bash
    traceroute example.com
    ```

2. Maksimum 15 sıçrama ile traceroute:
    ```bash
    traceroute -m 15 example.com
    ```

3. IP adreslerini çözümlemeden traceroute:
    ```bash
    traceroute -n example.com
    ```

4. Belirli bir port üzerinden traceroute:
    ```bash
    traceroute -p 80 example.com
    ```

5. Her bir sıçrama için 2 saniye bekleyerek traceroute:
    ```bash
    traceroute -w 2 example.com
    ```

## İpuçları
- Ağ sorunlarını teşhis ederken, `-n` seçeneğini kullanarak daha hızlı sonuçlar alabilirsiniz.
- Hedefin yanıt vermediği durumlarda, `-m` seçeneği ile sıçrama sayısını artırmayı deneyin.
- Traceroute sonuçlarını analiz ederken, her bir sıçramanın yanıt süresini dikkate alarak ağın hangi kısmında sorun olabileceğini belirleyebilirsiniz.