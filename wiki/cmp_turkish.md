# [Türkçe] Debian Almquist Shell (dash) cmp Kullanımı: İki dosyayı karşılaştırma

## Genel Bakış
`cmp` komutu, iki dosyanın içeriğini karşılaştırmak için kullanılır. Bu komut, dosyaların ilk farklılıklarını bulur ve hangi baytların farklı olduğunu gösterir. Eğer dosyalar tamamen aynıysa, herhangi bir çıktı üretmez.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
cmp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Farklı baytların konumlarını ve değerlerini gösterir.
- `-s`: Sessiz modda çalışır; sadece dosyaların eşit olup olmadığını belirtir.
- `-i OFFSET`: Karşılaştırmaya belirli bir bayt konumundan başlar.
- `-n N`: Sadece ilk N baytı karşılaştırır.

## Yaygın Örnekler
Aşağıda `cmp` komutunun bazı pratik kullanımları verilmiştir:

### İki dosyayı karşılaştırma
```bash
cmp dosya1.txt dosya2.txt
```

### Farklı baytların konumlarını gösterme
```bash
cmp -l dosya1.txt dosya2.txt
```

### Sessiz modda karşılaştırma
```bash
cmp -s dosya1.txt dosya2.txt
if [ $? -eq 0 ]; then
    echo "Dosyalar eşit."
else
    echo "Dosyalar farklı."
fi
```

### Belirli bir bayttan karşılaştırma
```bash
cmp -i 10 dosya1.txt dosya2.txt
```

### İlk N baytı karşılaştırma
```bash
cmp -n 100 dosya1.txt dosya2.txt
```

## İpuçları
- `cmp` komutunu, dosyaların bütünlüğünü kontrol etmek için kullanabilirsiniz.
- Büyük dosyalarla çalışırken, `-n` seçeneği ile karşılaştırmayı hızlandırabilirsiniz.
- Farklılıkları daha iyi analiz etmek için `-l` seçeneğini kullanarak detaylı bilgi alabilirsiniz.