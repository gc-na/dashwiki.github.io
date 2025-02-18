# [Türkçe] Debian Almquist Shell (dash) pwd Kullanımı: Mevcut çalışma dizinini gösterir

## Genel Bakış
`pwd` (print working directory) komutu, kullanıcıya mevcut çalışma dizinini gösterir. Terminalde hangi dizinde bulunduğunuzu hızlıca öğrenmek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
pwd [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-L`: Mantıksal yol kullanarak mevcut dizini gösterir.
- `-P`: Fiziksel yol kullanarak mevcut dizini gösterir.

## Yaygın Örnekler
1. Basit bir `pwd` komutu ile mevcut dizini görüntüleme:
   ```bash
   pwd
   ```

2. Mantıksal yol ile mevcut dizini görüntüleme:
   ```bash
   pwd -L
   ```

3. Fiziksel yol ile mevcut dizini görüntüleme:
   ```bash
   pwd -P
   ```

## İpuçları
- `pwd` komutunu sık sık kullanarak, terminalde hangi dizinde çalıştığınızı hatırlamak kolaylaşır.
- Eğer birden fazla terminal penceresi açtıysanız, her birinde `pwd` komutunu kullanarak hangi dizinde olduğunuzu kontrol edebilirsiniz.
- `pwd` komutunu bir betik içinde kullanarak, betiğin çalıştığı dizini dinamik olarak öğrenebilirsiniz.