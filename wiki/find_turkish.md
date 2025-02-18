# [Debian] Debian Almquist Shell (dash) find Kullanımı: Dosya adlarını bulma

## Genel Bakış
`find` komutu, belirli bir dizin içinde dosya ve dizinleri aramak için kullanılır. Kullanıcıların dosya adlarına, türlerine, boyutlarına veya diğer özelliklerine göre arama yapmalarını sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
find [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-name`: Belirtilen adı taşıyan dosyaları bulur.
- `-type`: Dosya türünü belirtir (örneğin, `f` dosya, `d` dizin).
- `-size`: Belirtilen boyutta dosyaları bulur.
- `-mtime`: Dosyanın son değiştirilme tarihine göre arama yapar.
- `-exec`: Bulunan dosyalar üzerinde belirtilen komutu çalıştırır.

## Yaygın Örnekler
Aşağıda `find` komutunun bazı pratik örnekleri verilmiştir:

1. Belirli bir dizinde belirli bir dosya adını aramak:
   ```bash
   find /home/kullanici -name "belge.txt"
   ```

2. Tüm dizinlerde `.jpg` uzantılı dosyaları bulmak:
   ```bash
   find / -name "*.jpg"
   ```

3. 100 MB'den büyük dosyaları bulmak:
   ```bash
   find / -size +100M
   ```

4. Son 7 gün içinde değiştirilmiş dosyaları bulmak:
   ```bash
   find /home/kullanici -mtime -7
   ```

5. Bulunan dosyaları silmek için `-exec` kullanmak:
   ```bash
   find /tmp -name "*.tmp" -exec rm {} \;
   ```

## İpuçları
- `find` komutunu kullanırken, arama alanını daraltmak için dizinleri belirlemek, arama süresini kısaltabilir.
- `-print` seçeneği, bulunan dosyaların adlarını ekrana yazdırmak için kullanılabilir; ancak bu, varsayılan olarak etkin olduğu için genellikle belirtilmesine gerek yoktur.
- `-maxdepth` seçeneği ile arama derinliğini sınırlayarak daha hızlı sonuçlar elde edebilirsiniz. Örneğin, sadece birinci seviyedeki dosyaları bulmak için:
  ```bash
  find /home/kullanici -maxdepth 1
  ```