# [Türkçe] Debian Almquist Shell (dash) test Kullanımı: Koşul testleri yapar

## Genel Bakış
`test` komutu, belirli koşulları kontrol etmek için kullanılan bir komuttur. Dosya varlığı, dosya türü, sayısal karşılaştırmalar gibi çeşitli durumları test edebilir. Bu komut, genellikle koşullu ifadelerde ve betiklerde kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
test [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Belirtilen dosyanın var olup olmadığını kontrol eder.
- `-f`: Belirtilen dosyanın bir dosya olup olmadığını kontrol eder.
- `-d`: Belirtilen dosyanın bir dizin olup olmadığını kontrol eder.
- `-z`: Belirtilen stringin boş olup olmadığını kontrol eder.
- `-eq`: İki sayının eşit olup olmadığını kontrol eder.
- `-ne`: İki sayının eşit olmadığını kontrol eder.

## Yaygın Örnekler
Aşağıda `test` komutunun bazı pratik örnekleri bulunmaktadır:

### Dosya Varlığını Kontrol Etme
```bash
test -e /path/to/file && echo "Dosya mevcut"
```

### Dosya Türünü Kontrol Etme
```bash
test -f /path/to/file && echo "Bu bir dosya"
test -d /path/to/directory && echo "Bu bir dizin"
```

### String Boşluğunu Kontrol Etme
```bash
string="merhaba"
test -z "$string" && echo "String boş" || echo "String dolu"
```

### Sayısal Karşılaştırma
```bash
a=5
b=10
test $a -lt $b && echo "$a, $b'den küçüktür"
```

## İpuçları
- `test` komutunu kullanırken, koşul ifadelerini daha okunabilir hale getirmek için `[` ve `]` köşeli parantezleri kullanabilirsiniz. Örneğin: `[ -e /path/to/file ]`.
- `test` komutunu `&&` ve `||` ile birleştirerek daha karmaşık koşullu ifadeler oluşturabilirsiniz.
- Betiklerinizde `test` komutunu kullanırken, her zaman doğru dosya yollarını ve argümanları kontrol edin.