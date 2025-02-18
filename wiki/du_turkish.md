# [Türkçe] Debian Almquist Shell (dash) du: Dosya ve dizin boyutlarını gösterir

## Genel Bakış
`du` (disk usage) komutu, dosya ve dizinlerin disk üzerindeki kullanım alanını gösterir. Bu komut, sistem yöneticileri ve kullanıcılar için disk alanını yönetmek ve analiz etmek amacıyla oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
du [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: İnsan tarafından okunabilir formatta boyutları gösterir (örneğin, KB, MB).
- `-s`: Toplam boyutu yalnızca bir kez gösterir, alt dizinleri listelemez.
- `-a`: Tüm dosyaların ve dizinlerin boyutlarını gösterir.
- `-c`: Toplam boyutları hesaplar ve en sonunda toplamı gösterir.

## Yaygın Örnekler
1. Belirli bir dizinin boyutunu gösterme:
   ```bash
   du -sh /path/to/directory
   ```

2. Tüm dosya ve dizinlerin boyutlarını listeleme:
   ```bash
   du -ah /path/to/directory
   ```

3. Dizinlerin boyutlarını toplamda gösterme:
   ```bash
   du -sc /path/to/directory/*
   ```

4. Belirli bir dizindeki dosyaların boyutlarını gösterme:
   ```bash
   du -h /path/to/directory/*.txt
   ```

## İpuçları
- `du` komutunu `sort` ile birleştirerek en büyük dosyaları veya dizinleri bulabilirsiniz:
  ```bash
  du -ah /path/to/directory | sort -rh | head -n 10
  ```
- Disk kullanımını daha iyi analiz etmek için `ncdu` gibi araçları kullanmayı düşünebilirsiniz; bu, etkileşimli bir arayüz sunar.
- Dizinlerin boyutlarını kontrol etmek için düzenli aralıklarla `du` komutunu çalıştırmak, disk alanı yönetimi açısından faydalı olabilir.