# [Türkçe] Debian Almquist Shell (dash) rmdir Kullanımı: Boş dizinleri silme komutu

## Genel Bakış
`rmdir` komutu, boş dizinleri silmek için kullanılır. Eğer dizin içinde dosya veya alt dizin varsa, bu komut çalışmaz ve hata verir.

## Kullanım
Temel sözdizimi şu şekildedir:
```
rmdir [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `--ignore-fail-on-non-empty`: Dizin boş değilse hata vermeden devam eder.
- `--verbose`: Silme işlemi sırasında daha fazla bilgi verir.

## Yaygın Örnekler
- Boş bir dizini silmek için:
  ```bash
  rmdir /path/to/empty-directory
  ```

- Birden fazla boş dizini aynı anda silmek için:
  ```bash
  rmdir /path/to/empty-directory1 /path/to/empty-directory2
  ```

- Hata mesajlarını görmezden gelmek için:
  ```bash
  rmdir --ignore-fail-on-non-empty /path/to/directory
  ```

- Silme işlemi sırasında bilgi almak için:
  ```bash
  rmdir --verbose /path/to/empty-directory
  ```

## İpuçları
- `rmdir` komutunu kullanmadan önce dizinin gerçekten boş olduğundan emin olun.
- Eğer dizin içinde dosya varsa, `rmdir` yerine `rm -r` komutunu kullanarak dizini ve içeriğini silebilirsiniz.
- Dizin silme işlemi geri alınamaz, bu yüzden dikkatli olun.