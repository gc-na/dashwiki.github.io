# [Türkçe] Debian Almquist Shell (dash) uname Kullanımı: Sistem bilgilerini görüntüleme

## Genel Bakış
`uname` komutu, işletim sistemi hakkında bilgi sağlayan bir komuttur. Bu komut, sistemin çekirdek adı, sürüm bilgisi ve mimarisi gibi çeşitli bilgileri görüntülemenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
uname [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bilgileri bir arada gösterir.
- `-s`: Çekirdek adını gösterir.
- `-n`: Ağ ana bilgisayar adını gösterir.
- `-r`: Çekirdek sürümünü gösterir.
- `-v`: Çekirdek sürüm bilgilerini gösterir.
- `-m`: Sistem mimarisini gösterir.

## Yaygın Örnekler
Aşağıda `uname` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### Tüm Bilgileri Gösterme
```
uname -a
```

### Çekirdek Adını Gösterme
```
uname -s
```

### Çekirdek Sürümünü Gösterme
```
uname -r
```

### Sistem Mimarisi Gösterme
```
uname -m
```

## İpuçları
- `uname -a` komutunu kullanarak sisteminiz hakkında kapsamlı bilgi alabilirsiniz.
- Belirli bir bilgiye ihtiyaç duyuyorsanız, yalnızca gerekli seçeneği kullanarak daha hızlı sonuçlar elde edebilirsiniz.
- Komutları bir betik içinde kullanarak sistem bilgilerini otomatik olarak kaydedebilirsiniz.