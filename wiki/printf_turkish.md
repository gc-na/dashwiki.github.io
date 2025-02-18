# [Türkçe] Debian Almquist Shell (dash) printf Kullanımı: Formatlı çıktı üretme

## Genel Bakış
`printf` komutu, formatlı metin çıktısı üretmek için kullanılır. C dilindeki `printf` fonksiyonuna benzer bir şekilde çalışır ve kullanıcıların belirli bir formatta verileri ekrana yazdırmasına olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:

```
printf [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-v`: Değişken olarak çıktı üretir.
- `-f`: Format belirler.
- `-n`: Yeni satır karakteri eklemez.

## Yaygın Örnekler
Aşağıda `printf` komutunun bazı pratik örnekleri bulunmaktadır:

### Basit Metin Yazdırma
```sh
printf "Merhaba, Dünya!\n"
```

### Değişken Kullanımı
```sh
isim="Ahmet"
printf "Merhaba, %s!\n" "$isim"
```

### Sayı Formatlama
```sh
printf "Sayı: %.2f\n" 3.14159
```

### Birden Fazla Argüman
```sh
printf "%s, %s!\n" "Merhaba" "Dünya"
```

## İpuçları
- Format dizelerini dikkatlice oluşturun; `%s` metin, `%d` tam sayı ve `%.2f` gibi ifadelerle sayıları doğru formatlayabilirsiniz.
- Çıktıyı daha okunabilir hale getirmek için boşluk ve yeni satır karakterlerini kullanmayı unutmayın.
- Hataları önlemek için her zaman değişkenlerinizi tırnak içinde kullanın.