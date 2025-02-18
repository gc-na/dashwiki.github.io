# [Türkçe] Debian Almquist Shell (dash) tee Kullanımı: Verileri birden fazla yere yönlendirme

## Genel Bakış
`tee` komutu, standart girdi verilerini okur ve bu verileri hem ekrana yazdırır hem de belirtilen dosyalara kaydeder. Bu, verilerin birden fazla yere yönlendirilmesi gerektiğinde oldukça kullanışlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
tee [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`, `--append`: Verileri dosyaya ekler, mevcut içeriği silmez.
- `-i`, `--ignore-interrupts`: Kesme sinyallerini yok sayar.
- `--help`: Komut hakkında yardım bilgilerini gösterir.
- `--version`: `tee` komutunun sürüm bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `tee` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Temel Kullanım**: Bir dosyaya veri yazma ve aynı zamanda ekrana yazdırma.
   ```bash
   echo "Merhaba Dünya" | tee dosya.txt
   ```

2. **Verileri Ekleme**: Mevcut bir dosyaya veri eklemek için.
   ```bash
   echo "Yeni Satır" | tee -a dosya.txt
   ```

3. **Birden Fazla Dosyaya Yazma**: Verileri birden fazla dosyaya yönlendirme.
   ```bash
   echo "Veri" | tee dosya1.txt dosya2.txt
   ```

4. **Hata Ayıklama**: Bir komutun çıktısını hem dosyaya hem de ekrana yazdırma.
   ```bash
   ls -l | tee liste.txt
   ```

## İpuçları
- `tee` komutunu bir boru hattı içinde kullanarak, bir komutun çıktısını hem dosyaya kaydedebilir hem de başka bir komuta yönlendirebilirsiniz.
- Dosya izinlerine dikkat edin; yazma izniniz olmayan bir dosyaya veri yazmaya çalışmak hata verecektir.
- `-a` seçeneğini kullanarak mevcut dosya içeriğini koruyarak veri eklemek, log dosyaları gibi sürekli güncellenen dosyalar için faydalıdır.