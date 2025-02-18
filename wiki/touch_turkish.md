# [Türkçe] Debian Almquist Shell (dash) touch Kullanımı: Dosya zaman damgalarını güncelleme

## Genel Bakış
`touch` komutu, dosyaların zaman damgalarını güncellemek veya yeni boş dosyalar oluşturmak için kullanılır. Eğer belirtilen dosya mevcut değilse, `touch` komutu yeni bir dosya oluşturur; mevcutsa, dosyanın erişim ve değiştirilme zamanlarını günceller.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
touch [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Sadece erişim zamanını günceller.
- `-m`: Sadece değiştirilme zamanını günceller.
- `-c`: Dosya mevcut değilse oluşturmaz, yalnızca mevcut dosyanın zaman damgalarını günceller.
- `-d <tarih>`: Belirtilen tarih ve saat ile zaman damgalarını günceller.
- `-t <tarih>`: Belirtilen tarih ve saat formatında zaman damgalarını günceller.

## Yaygın Örnekler
Aşağıda `touch` komutunun bazı pratik örnekleri verilmiştir:

### Yeni Bir Boş Dosya Oluşturma
```bash
touch yeni_dosya.txt
```

### Mevcut Bir Dosyanın Zaman Damgalarını Güncelleme
```bash
touch mevcut_dosya.txt
```

### Sadece Erişim Zamanını Güncelleme
```bash
touch -a mevcut_dosya.txt
```

### Sadece Değiştirilme Zamanını Güncelleme
```bash
touch -m mevcut_dosya.txt
```

### Belirli Bir Tarih ile Zaman Damgalarını Güncelleme
```bash
touch -d "2023-10-01 12:00" mevcut_dosya.txt
```

### Dosya Oluşmadan Güncelleme Yapmama
```bash
touch -c olmayan_dosya.txt
```

## İpuçları
- `touch` komutunu sık sık kullanıyorsanız, dosya zaman damgalarını güncellemek için bir alias oluşturmayı düşünebilirsiniz.
- Dosya oluşturma işlemleri için `-c` seçeneğini kullanarak yanlışlıkla dosya oluşturma riskini azaltabilirsiniz.
- Zaman damgalarını güncellerken tarih formatına dikkat edin; yanlış bir format hata almanıza neden olabilir.