# [Türkçe] Debian Almquist Shell (dash) mkdir Kullanımı: Dizin oluşturma komutu

## Genel Bakış
`mkdir` komutu, belirtilen isimle yeni dizinler (kataloglar) oluşturmak için kullanılır. Bu komut, dosya sisteminde düzen sağlamak ve yeni projeler için gerekli dizin yapısını kurmak amacıyla oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
mkdir [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Ara dizinleri oluşturur. Yani, belirtilen yolun içindeki eksik dizinleri otomatik olarak oluşturur.
- `-m`: Oluşturulan dizinin izinlerini belirler. Örneğin, `-m 755` ile izinleri ayarlayabilirsiniz.
- `--help`: Komutun kullanımına dair yardım bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `mkdir` komutunun bazı pratik örnekleri bulunmaktadır:

### Basit Dizin Oluşturma
Yeni bir dizin oluşturmak için:
```bash
mkdir yeni_dizin
```

### Birden Fazla Dizin Oluşturma
Birden fazla dizin oluşturmak için:
```bash
mkdir dizin1 dizin2 dizin3
```

### Ara Dizinlerle Dizin Oluşturma
Eksik ara dizinlerle birlikte dizin oluşturmak için:
```bash
mkdir -p ana_dizin/alt_dizin/alt_alt_dizin
```

### Belirli İzinlerle Dizin Oluşturma
Dizini belirli izinlerle oluşturmak için:
```bash
mkdir -m 755 yeni_dizin
```

## İpuçları
- Dizin oluştururken, dizin adlarının geçerli karakterler içerdiğinden emin olun.
- `-p` seçeneğini kullanarak, karmaşık dizin yapıları oluştururken hata yapma olasılığınızı azaltabilirsiniz.
- Dizin oluşturduktan sonra, `ls` komutunu kullanarak oluşturduğunuz dizinleri kontrol edebilirsiniz.