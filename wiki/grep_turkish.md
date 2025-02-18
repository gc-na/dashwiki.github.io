# [Türkçe] Debian Almquist Shell (dash) grep Kullanımı: Metin içinde desen arama

## Genel Bakış
`grep` komutu, metin dosyaları içinde belirli bir desen veya kelime grubu aramak için kullanılır. Bu komut, özellikle büyük dosyalarda veya çıktıların filtrelenmesinde oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
grep [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Büyük/küçük harf duyarsız arama yapar.
- `-v`: Deseni içermeyen satırları gösterir.
- `-r`: Alt dizinlerdeki dosyalarla birlikte, dizin içinde arama yapar.
- `-n`: Eşleşen satırların numaralarını gösterir.
- `-l`: Eşleşen dosya adlarını listeler.

## Yaygın Örnekler
Aşağıda `grep` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir kelimeyi bir dosyada arama:
   ```bash
   grep "kelime" dosya.txt
   ```

2. Büyük/küçük harf duyarsız arama:
   ```bash
   grep -i "kelime" dosya.txt
   ```

3. Eşleşmeyen satırları gösterme:
   ```bash
   grep -v "kelime" dosya.txt
   ```

4. Dizin içinde arama yapma:
   ```bash
   grep -r "kelime" /path/to/directory
   ```

5. Eşleşen satırların numaralarını gösterme:
   ```bash
   grep -n "kelime" dosya.txt
   ```

## İpuçları
- `grep` komutunu `|` (pipe) ile diğer komutlarla birleştirerek daha karmaşık aramalar yapabilirsiniz.
- Çok sayıda dosyada arama yaparken, sonuçları daha iyi yönetmek için `-l` seçeneğini kullanarak sadece dosya adlarını listeleyebilirsiniz.
- Arama sonuçlarını daha okunabilir hale getirmek için `--color` seçeneğini ekleyerek eşleşen kelimeleri renklendirebilirsiniz.