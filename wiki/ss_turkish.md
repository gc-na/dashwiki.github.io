# [Türkçe] Debian Almquist Shell (dash) ss Kullanımı: Ağ soketlerini görüntüleme

## Genel Bakış
`ss` komutu, sistemdeki ağ soketleri hakkında bilgi almak için kullanılır. Bu komut, aktif bağlantıları, dinleyen soketleri ve diğer ağ ile ilgili bilgileri hızlı bir şekilde görüntülemenizi sağlar.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
ss [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-t`: TCP bağlantılarını gösterir.
- `-u`: UDP bağlantılarını gösterir.
- `-l`: Dinleyen soketleri listeler.
- `-p`: Soketlerin hangi süreçler tarafından kullanıldığını gösterir.
- `-n`: Adres ve port numaralarını sayısal olarak gösterir.

## Yaygın Örnekler
Aşağıda `ss` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm aktif TCP bağlantılarını listelemek için:
   ```bash
   ss -t
   ```

2. Dinleyen soketleri görüntülemek için:
   ```bash
   ss -l
   ```

3. UDP bağlantılarını listelemek için:
   ```bash
   ss -u
   ```

4. Belirli bir portta dinleyen soketleri bulmak için:
   ```bash
   ss -ltn 'sport = :80'
   ```

5. Soketlerin hangi süreçler tarafından kullanıldığını görmek için:
   ```bash
   ss -p
   ```

## İpuçları
- `ss` komutunu kullanırken, `-n` seçeneğini eklemek, adreslerin ve portların sayısal olarak gösterilmesini sağlar, bu da daha hızlı bir çıktı almanıza yardımcı olur.
- Ağ sorunlarını teşhis etmek için `ss` komutunu kullanarak hangi soketlerin açık olduğunu ve hangi süreçlerin bu soketleri kullandığını kontrol edebilirsiniz.
- `ss` komutunu düzenli olarak kullanarak sisteminizdeki ağ bağlantılarını izlemek, güvenlik ve performans açısından faydalı olabilir.