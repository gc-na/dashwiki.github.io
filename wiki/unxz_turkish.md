# [Türkçe] Debian Almquist Shell (dash) unxz Kullanımı: Sıkıştırılmış dosyaları açma

## Genel Bakış
`unxz` komutu, `.xz` uzantılı sıkıştırılmış dosyaları açmak için kullanılır. Bu komut, XZ sıkıştırma formatını destekler ve dosyaların boyutunu küçültmek için yaygın olarak kullanılır. `unxz`, dosyayı açarak orijinal haline geri döndürür.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
unxz [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-k`, `--keep`: Sıkıştırılmış dosyayı açtıktan sonra orijinal dosyayı korur.
- `-f`, `--force`: Var olan dosyaların üzerine yazmak için zorlar.
- `-v`, `--verbose`: İşlem sırasında daha fazla bilgi verir.

## Yaygın Örnekler
Aşağıda `unxz` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Basit bir dosyayı açma
```bash
unxz dosya.xz
```

### Örnek 2: Orijinal dosyayı koruyarak açma
```bash
unxz -k dosya.xz
```

### Örnek 3: Var olan dosyaların üzerine yazma
```bash
unxz -f dosya.xz
```

### Örnek 4: İşlem sırasında bilgi alma
```bash
unxz -v dosya.xz
```

## İpuçları
- Sıkıştırılmış dosyaları açmadan önce, dosyanın yedeğini almak iyi bir uygulamadır.
- `-k` seçeneğini kullanarak orijinal dosyayı kaybetmeden açabilirsiniz.
- Eğer sıkıştırılmış dosyanızın boyutu çok büyükse, açma işlemi biraz zaman alabilir; bu yüzden sabırlı olun.