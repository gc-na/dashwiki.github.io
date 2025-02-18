# [Türkçe] Debian Almquist Shell (dash) uniq Kullanımı: Tekil satırları gösterir

## Genel Bakış
`uniq` komutu, bir dosyada veya standart girişteki ardışık tekrar eden satırları kaldırarak yalnızca benzersiz satırları gösterir. Genellikle, sıralı verilerle birlikte kullanılır, çünkü `uniq` yalnızca ardışık tekrarları kaldırır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
uniq [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c`: Her benzersiz satırın önüne tekrar sayısını ekler.
- `-d`: Sadece tekrar eden satırları gösterir.
- `-u`: Sadece benzersiz (tekrar etmeyen) satırları gösterir.
- `-i`: Büyük/küçük harf duyarsız olarak karşılaştırma yapar.

## Yaygın Örnekler
Aşağıda `uniq` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Basit Kullanım**: Bir dosyadaki benzersiz satırları gösterme.
   ```bash
   uniq dosya.txt
   ```

2. **Tekrar Sayısı ile Gösterme**: Her benzersiz satırın önüne tekrar sayısını ekleme.
   ```bash
   uniq -c dosya.txt
   ```

3. **Sadece Tekrar Eden Satırları Gösterme**:
   ```bash
   uniq -d dosya.txt
   ```

4. **Benzersiz Satırları Gösterme**:
   ```bash
   uniq -u dosya.txt
   ```

5. **Büyük/Küçük Harf Duyarsız Kullanım**:
   ```bash
   uniq -i dosya.txt
   ```

## İpuçları
- `uniq` komutunu kullanmadan önce verilerinizi sıralamak, daha doğru sonuçlar elde etmenizi sağlar. Bunu `sort` komutuyla yapabilirsiniz.
- Uzun dosyalar üzerinde çalışırken, `-c` seçeneği ile hangi satırların ne kadar tekrar ettiğini görmek faydalı olabilir.
- `uniq` komutunu bir boru (pipe) ile diğer komutlarla birleştirerek daha karmaşık işlemler gerçekleştirebilirsiniz. Örneğin, `cat dosya.txt | sort | uniq` komutuyla dosyadaki benzersiz satırları sıralı bir şekilde görebilirsiniz.