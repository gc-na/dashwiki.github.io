# [Türkçe] Debian Almquist Shell (dash) comm komutu: İki dosya arasındaki farklılıkları karşılaştırma

## Genel Bakış
`comm` komutu, iki sıralı dosya arasındaki satırları karşılaştırarak, her dosyada bulunan ve her iki dosyada da bulunmayan satırları gösterir. Bu komut, özellikle metin dosyalarının içeriklerini analiz etmek ve farklılıkları belirlemek için kullanışlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
comm [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-1`: İlk dosyada bulunan ancak ikinci dosyada bulunmayan satırları gizler.
- `-2`: İkinci dosyada bulunan ancak ilk dosyada bulunmayan satırları gizler.
- `-3`: Her iki dosyada da bulunan satırları gizler.
- `-i`: Karşılaştırma sırasında büyük/küçük harf duyarlılığını göz ardı eder.

## Yaygın Örnekler
Aşağıda `comm` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: İki dosya arasındaki farkları gösterme
```bash
comm dosya1.txt dosya2.txt
```
Bu komut, `dosya1.txt` ve `dosya2.txt` dosyaları arasındaki farkları gösterir.

### Örnek 2: Sadece birinci dosyada bulunan satırları gösterme
```bash
comm -13 dosya1.txt dosya2.txt
```
Bu komut, yalnızca `dosya1.txt` dosyasında bulunan satırları gösterir.

### Örnek 3: Büyük/küçük harf duyarlılığını göz ardı ederek karşılaştırma yapma
```bash
comm -i dosya1.txt dosya2.txt
```
Bu komut, iki dosyayı büyük/küçük harf duyarlılığına bakmadan karşılaştırır.

## İpuçları
- Dosyaların sıralı olduğundan emin olun; `comm` komutu, dosyaların sıralı olmaması durumunda beklenmeyen sonuçlar verebilir. Gerekirse `sort` komutunu kullanarak dosyaları sıralayın.
- Farklılıkları daha iyi anlamak için `comm` çıktısını `less` veya `more` gibi bir sayfalayıcı ile görüntüleyebilirsiniz.
- Çok büyük dosyalarla çalışıyorsanız, `comm` komutunun çıktısını bir dosyaya yönlendirmek, sonuçları daha sonra incelemek için faydalı olabilir. Örneğin: 
```bash
comm dosya1.txt dosya2.txt > farklar.txt
```