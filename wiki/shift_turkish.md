# [Türkçe] Debian Almquist Shell (dash) shift Kullanımı: Argümanları sola kaydırma

## Genel Bakış
`shift` komutu, kabuk betiklerinde argümanları sola kaydırmak için kullanılır. Bu, komut satırında geçirilen argümanların sıralamasını değiştirmeye yarar. Özellikle birden fazla argümanla çalışırken, belirli bir argümanı işlemek için diğerlerini kaydırmak faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
shift [options] [arguments]
```

## Yaygın Seçenekler
- `n`: Argümanları n kadar sola kaydırır. Eğer n belirtilmezse, varsayılan olarak 1 kaydırma yapılır.

## Yaygın Örnekler

### Örnek 1: Basit Kaydırma
Aşağıdaki komut, ilk argümanı kaydırır ve ikinci argümanı ilk argüman olarak alır.

```sh
#!/bin/dash
set -- arg1 arg2 arg3
echo "Önce: $1"  # Çıktı: Önce: arg1
shift
echo "Sonra: $1" # Çıktı: Sonra: arg2
```

### Örnek 2: Çoklu Kaydırma
Aşağıdaki örnekte, iki argümanı sola kaydırıyoruz.

```sh
#!/bin/dash
set -- arg1 arg2 arg3 arg4
echo "Önce: $1"  # Çıktı: Önce: arg1
shift 2
echo "Sonra: $1" # Çıktı: Sonra: arg3
```

### Örnek 3: Argüman Kontrolü
Argüman sayısını kontrol edip kaydırma işlemi yapma:

```sh
#!/bin/dash
set -- arg1 arg2 arg3
if [ $# -gt 1 ]; then
    shift
fi
echo "Sonuç: $1" # Çıktı: Sonuç: arg2
```

## İpuçları
- `shift` komutunu kullanmadan önce argüman sayısını kontrol etmek, hata önlemek için iyi bir uygulamadır.
- Birden fazla argümanı kaydırmak için `shift n` kullanarak işlemi hızlandırabilirsiniz.
- `shift` komutunu döngüler içinde kullanarak argümanları sırayla işlemek oldukça etkilidir.