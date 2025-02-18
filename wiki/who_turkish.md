# [Türkçe] Debian Almquist Shell (dash) who komutu: Kullanıcı oturumlarını görüntüleme

## Genel Bakış
`who` komutu, sistemde oturum açmış kullanıcıların listesini görüntülemek için kullanılır. Bu komut, kullanıcı adı, oturum açma zamanı ve terminal bilgileri gibi bilgileri sağlar.

## Kullanım
Temel sözdizimi şu şekildedir:

```
who [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-b`: Sistemin en son yeniden başlatıldığı zamanı gösterir.
- `-q`: Sadece kullanıcı adlarını ve toplam kullanıcı sayısını gösterir.
- `-H`: Başlık satırını gösterir.

## Yaygın Örnekler
Aşağıda `who` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Sistemdeki tüm oturum açmış kullanıcıları görüntüleme:
   ```bash
   who
   ```

2. Sistemin en son ne zaman yeniden başlatıldığını gösterme:
   ```bash
   who -b
   ```

3. Sadece kullanıcı adlarını ve toplam kullanıcı sayısını görüntüleme:
   ```bash
   who -q
   ```

4. Başlık satırı ile kullanıcı bilgilerini görüntüleme:
   ```bash
   who -H
   ```

## İpuçları
- `who` komutunu sık sık kullanarak sistemdeki aktif kullanıcıları takip edebilirsiniz.
- Eğer belirli bir kullanıcı hakkında daha fazla bilgi almak isterseniz, `w` komutunu kullanabilirsiniz; bu komut, kullanıcıların hangi işlemleri yaptığını da gösterir.
- `who` çıktısını bir dosyaya yönlendirmek için `>` operatörünü kullanarak bilgileri kaydedebilirsiniz:
  ```bash
  who > kullanicilar.txt
  ```