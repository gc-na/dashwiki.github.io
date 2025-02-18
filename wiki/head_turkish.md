# [Türkçe] Debian Almquist Shell (dash) head Kullanımı: Dosya içeriğinin başını gösterir

## Genel Bakış
`head` komutu, bir dosyanın başlangıcındaki belirli sayıda satırı görüntülemek için kullanılır. Genellikle büyük dosyaların içeriğini hızlıca gözden geçirmek için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
head [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n [sayı]`: Görüntülenecek satır sayısını belirtir. Varsayılan olarak ilk 10 satırı gösterir.
- `-c [bayt]`: Görüntülenecek bayt sayısını belirtir.
- `-q`: Birden fazla dosya görüntüleniyorsa, dosya başlıklarını göstermez.
- `-v`: Her dosya için başlık bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `head` komutunun bazı pratik örnekleri bulunmaktadır:

1. İlk 10 satırı görüntüleme:
   ```bash
   head dosya.txt
   ```

2. İlk 5 satırı görüntüleme:
   ```bash
   head -n 5 dosya.txt
   ```

3. İlk 20 baytı görüntüleme:
   ```bash
   head -c 20 dosya.txt
   ```

4. Birden fazla dosyanın başını görüntüleme:
   ```bash
   head dosya1.txt dosya2.txt
   ```

5. Her dosya için başlık bilgilerini göstererek görüntüleme:
   ```bash
   head -v dosya1.txt dosya2.txt
   ```

## İpuçları
- Büyük dosyalarla çalışırken, `head` komutunu kullanarak dosyanın içeriğini hızlıca kontrol edebilirsiniz.
- `-n` seçeneği ile istediğiniz satır sayısını belirleyerek daha fazla esneklik sağlayabilirsiniz.
- Eğer dosya başlıklarını görmek istemiyorsanız, `-q` seçeneğini kullanarak çıktıyı daha temiz hale getirebilirsiniz.