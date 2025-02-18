# [Türkçe] Debian Almquist Shell (dash) diff Kullanımı: İki dosya arasındaki farkları karşılaştırma

## Genel Bakış
`diff` komutu, iki dosya arasındaki farklılıkları karşılaştırmak için kullanılır. Bu komut, dosyaların içeriğindeki değişiklikleri, eklemeleri veya silmeleri belirlemek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
diff [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u`: Birleştirilmiş çıktı formatında gösterir.
- `-i`: Büyük/küçük harf duyarsız karşılaştırma yapar.
- `-w`: Boşlukları göz ardı eder.
- `-q`: Sadece dosyaların farklı olup olmadığını bildirir.

## Yaygın Örnekler
Aşağıda `diff` komutunun bazı pratik örnekleri bulunmaktadır:

1. İki dosya arasındaki farkları gösterme:
   ```bash
   diff dosya1.txt dosya2.txt
   ```

2. Birleştirilmiş formatta farkları gösterme:
   ```bash
   diff -u dosya1.txt dosya2.txt
   ```

3. Büyük/küçük harf duyarsız karşılaştırma yapma:
   ```bash
   diff -i dosya1.txt dosya2.txt
   ```

4. Sadece dosyaların farklı olup olmadığını kontrol etme:
   ```bash
   diff -q dosya1.txt dosya2.txt
   ```

## İpuçları
- `diff` komutunu kullanırken, dosyaların aynı dizinde olduğundan emin olun; aksi takdirde, tam yolunu belirtmeniz gerekebilir.
- Farklılıkları daha iyi anlamak için `-u` seçeneğini kullanarak birleştirilmiş formatta çıktı almayı tercih edin.
- `diff` çıktısını bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  diff dosya1.txt dosya2.txt > farklar.txt
  ```