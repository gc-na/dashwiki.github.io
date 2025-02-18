# [Türkçe] Debian Almquist Shell (dash) date komutu: [tarih ve saat gösterimi]

## Genel Bakış
`date` komutu, sistemin tarih ve saat bilgilerini görüntülemek ve gerektiğinde bu bilgileri biçimlendirmek için kullanılır. Bu komut, kullanıcıların sistem zamanını kontrol etmelerine ve belirli bir formatta tarih ve saat bilgisi almalarına olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
date [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `+FORMAT`: Tarih ve saati belirtilen formatta gösterir.
- `-u`: UTC (Koordinatlı Evrensel Zaman) saat diliminde tarih ve saat gösterir.
- `-d STRING`: Belirtilen bir tarih ve saat dizesini kullanarak tarih ve saat bilgisi gösterir.

## Yaygın Örnekler
Aşağıda `date` komutunun bazı pratik örnekleri verilmiştir:

1. **Mevcut tarihi ve saati gösterme:**
   ```bash
   date
   ```

2. **Belirli bir formatta tarih ve saat gösterme:**
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. **UTC saat diliminde tarih ve saat gösterme:**
   ```bash
   date -u
   ```

4. **Belirli bir tarih ve saat dizesini kullanarak tarih gösterme:**
   ```bash
   date -d "2023-10-01 12:00:00"
   ```

5. **Bugünün tarihini sadece gün olarak gösterme:**
   ```bash
   date "+%d"
   ```

## İpuçları
- Tarih ve saat formatlarını özelleştirirken, `man date` komutunu kullanarak daha fazla bilgi edinebilirsiniz.
- `date` komutunu bir betik içinde kullanarak otomatik tarih ve saat bilgisi alabilirsiniz.
- Farklı tarih ve saat formatları denemek için `+FORMAT` seçeneğini kullanarak kişisel ihtiyaçlarınıza uygun çıktılar elde edebilirsiniz.