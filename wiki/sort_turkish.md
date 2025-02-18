# [Türkçe] Debian Almquist Shell (dash) sort Kullanımı: Dosya içeriğini sıralama

## Genel Bakış
`sort` komutu, bir dosyanın içeriğini sıralamak için kullanılır. Bu komut, metin dosyalarındaki satırları belirli bir düzene göre (alfabetik veya sayısal) sıralayarak yeni bir çıktı oluşturur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
sort [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-r`: Sıralamayı tersine çevirir.
- `-n`: Sayısal sıralama yapar.
- `-k`: Belirli bir alanı (kolonu) kullanarak sıralama yapar.
- `-u`: Tekrar eden satırları kaldırarak yalnızca benzersiz satırları gösterir.

## Yaygın Örnekler
Aşağıda `sort` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Basit Sıralama**
   Bir dosyanın içeriğini alfabetik olarak sıralamak için:
   ```bash
   sort dosya.txt
   ```

2. **Ters Sıralama**
   Bir dosyanın içeriğini ters alfabetik olarak sıralamak için:
   ```bash
   sort -r dosya.txt
   ```

3. **Sayısal Sıralama**
   Sayı içeren bir dosyanın içeriğini sayısal olarak sıralamak için:
   ```bash
   sort -n sayilar.txt
   ```

4. **Belirli Bir Alan Üzerinden Sıralama**
   İkinci alanı kullanarak sıralamak için:
   ```bash
   sort -k 2 dosya.txt
   ```

5. **Benzersiz Satırları Gösterme**
   Tekrar eden satırları kaldırarak sıralamak için:
   ```bash
   sort -u dosya.txt
   ```

## İpuçları
- Sıralama işlemi yapmadan önce dosyanızın yedeğini almak iyi bir uygulamadır.
- Sıralama işlemi sırasında büyük/küçük harf duyarlılığına dikkat edin; `-f` seçeneği ile bu durumu göz ardı edebilirsiniz.
- Birden fazla dosyayı sıralamak için dosya isimlerini arka arkaya yazabilirsiniz. Örneğin:
  ```bash
  sort dosya1.txt dosya2.txt
  ```