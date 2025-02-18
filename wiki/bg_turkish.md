# [Türkçe] Debian Almquist Shell (dash) bg Kullanımı: Arka planda bir işlemi çalıştırma

## Genel Bakış
`bg` komutu, bir işlemi arka planda çalıştırmak için kullanılır. Bu, kullanıcıya terminalde başka komutlar girmeye devam etme imkanı tanır. Genellikle, bir işlem duraklatıldığında ve arka planda çalıştırılmak istendiğinde kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
bg [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `job_id`: Arka planda çalıştırılacak olan duraklatılmış işlemin kimliği.
- `%n`: İşlem numarasını belirtir. Örneğin, `%1` birinci işlemi ifade eder.

## Yaygın Örnekler
Aşağıda `bg` komutunun bazı pratik örnekleri verilmiştir:

1. Duraklatılmış bir işlemi arka planda çalıştırma:
   ```bash
   bg %1
   ```

2. Tüm duraklatılmış işlemleri arka planda çalıştırma:
   ```bash
   bg
   ```

3. Belirli bir işlem kimliği ile arka planda çalıştırma:
   ```bash
   bg 1234
   ```

## İpuçları
- `jobs` komutunu kullanarak mevcut duraklatılmış işlemleri kontrol edebilirsiniz.
- İşlemi arka planda çalıştırmadan önce duraklatmak için `Ctrl + Z` tuş kombinasyonunu kullanın.
- Arka planda çalışan işlemleri yönetmek için `fg` komutunu kullanarak işlemi ön plana alabilirsiniz.