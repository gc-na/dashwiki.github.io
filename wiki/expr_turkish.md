# [Türkçe] Debian Almquist Shell (dash) expr Kullanımı: Matematiksel ifadeleri değerlendirme

## Overview
`expr` komutu, matematiksel ifadeleri değerlendirmek ve temel hesaplamalar yapmak için kullanılan bir komuttur. Bu komut, sayılar üzerinde toplama, çıkarma, çarpma ve bölme gibi işlemleri gerçekleştirebilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```sh
expr [options] [arguments]
```

## Common Options
- `-e`: İfade değerlendirmesi için kullanılır.
- `-s`: Sonuçları standart hata yerine standart çıkışa yazdırır.

## Common Examples
Aşağıda `expr` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Toplama
İki sayıyı toplamak için:

```sh
expr 5 + 3
```

### Çıkarma
İki sayı arasındaki farkı bulmak için:

```sh
expr 10 - 4
```

### Çarpma
İki sayıyı çarpmak için:

```sh
expr 7 \* 6
```

### Bölme
Bir sayıyı diğerine bölmek için:

```sh
expr 20 / 4
```

### Modül
Bir sayının diğerine bölümünden kalanı bulmak için:

```sh
expr 10 % 3
```

## Tips
- `expr` komutunda çarpma işlemi için `*` karakterini kullanmadan önce bir ters eğik çizgi (`\`) eklemeyi unutmayın.
- Daha karmaşık ifadeler için parantez kullanarak öncelik sırasını belirleyebilirsiniz.
- `expr` komutunun çıktısını değişkenlere atayarak daha karmaşık işlemler yapabilirsiniz. Örneğin:

```sh
result=$(expr 5 + 3)
echo "Sonuç: $result"
```