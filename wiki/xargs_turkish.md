# [Türkçe] Debian Almquist Shell (dash) xargs Kullanımı: Komutları argümanlarla birleştirir

## Genel Bakış
`xargs` komutu, standart girişten okunan verileri alarak bunları komut argümanları olarak kullanır. Bu, birden fazla dosya veya veri parçası ile işlem yaparken oldukça kullanışlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
xargs [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n N`: Her seferinde N argüman kullanarak komutu çalıştırır.
- `-d DELIMITER`: Giriş verilerini belirtilen ayırıcı ile ayırır.
- `-p`: Her komut çalıştırılmadan önce kullanıcıdan onay alır.
- `-0`: Null karakter ile biten girişleri işler (genellikle `find` ile birlikte kullanılır).

## Yaygın Örnekler
1. **Dosya silme**: `find` ile bulunan dosyaları silmek için:
   ```bash
   find . -name "*.tmp" | xargs rm
   ```

2. **Dosya içeriğini görüntüleme**: Belirli bir uzantıya sahip dosyaların içeriğini görüntülemek için:
   ```bash
   find . -name "*.txt" | xargs cat
   ```

3. **Belirli bir sayıda argüman ile komut çalıştırma**:
   ```bash
   echo "a b c d e f" | xargs -n 2 echo
   ```

4. **Kullanıcı onayı ile dosya silme**:
   ```bash
   find . -name "*.log" | xargs -p rm
   ```

## İpuçları
- `xargs` kullanırken, giriş verilerinin doğru bir şekilde ayrıldığından emin olun. Özellikle boşluk veya özel karakter içeren dosya adları için `-0` seçeneğini kullanmak faydalı olabilir.
- Geniş çaplı işlemler yapmadan önce `-p` seçeneği ile onay alarak yanlışlıkla veri kaybını önleyebilirsiniz.
- `xargs` ile birlikte `find` komutunu kullanmak, dosya işlemlerini daha verimli hale getirir.