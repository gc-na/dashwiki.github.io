# [Türkçe] Debian Almquist Shell (dash) rsync Kullanımı: Dosya senkronizasyonu

## Genel Bakış
`rsync`, dosyaları ve dizinleri yerel veya uzak bir sistem arasında senkronize etmek için kullanılan bir komuttur. Verimli bir şekilde yalnızca değişen verileri transfer ederek zaman ve bant genişliği tasarrufu sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
rsync [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Arşiv modu; dosyaların tüm özelliklerini (izinler, zaman damgaları, vb.) korur.
- `-v`: Ayrıntılı çıktı; işlemin ne yaptığını gösterir.
- `-z`: Verileri sıkıştırarak transfer eder, bu da bant genişliğinden tasarruf sağlar.
- `-r`: Alt dizinlerle birlikte dizinleri kopyalar.
- `--delete`: Hedef dizinde, kaynakta olmayan dosyaları siler.

## Yaygın Örnekler
1. Yerel bir dizinden başka bir dizine dosya kopyalama:
   ```bash
   rsync -av /kaynak/dizin/ /hedef/dizin/
   ```

2. Uzak bir sunucuya dosya kopyalama:
   ```bash
   rsync -av /yerel/dosya.txt kullanıcı@sunucu:/uzak/dizin/
   ```

3. Uzak bir sunucudan yerel bir dizine dosya indirme:
   ```bash
   rsync -av kullanıcı@sunucu:/uzak/dosya.txt /yerel/dizin/
   ```

4. Hedef dizinde kaynakta olmayan dosyaları silerek senkronizasyon yapma:
   ```bash
   rsync -av --delete /kaynak/dizin/ /hedef/dizin/
   ```

## İpuçları
- `-n` veya `--dry-run` seçeneğini kullanarak, gerçek transferi yapmadan önce nelerin kopyalanacağını görmek için bir önizleme yapabilirsiniz.
- Büyük dosyalarla çalışırken `-z` seçeneğini kullanarak transfer sırasında bant genişliğinden tasarruf edebilirsiniz.
- Sık sık senkronizasyon yapıyorsanız, bir betik oluşturup otomatikleştirmeyi düşünebilirsiniz.