# [Türkçe] Debian Almquist Shell (dash) kullanıcıları için kullanıcılar: Kullanıcı bilgilerini görüntüleme

## Genel Bakış
`users` komutu, sistemde oturum açmış olan kullanıcıların adlarını listelemek için kullanılır. Bu komut, birden fazla kullanıcı oturumu olduğunda hangi kullanıcıların aktif olduğunu hızlıca görmek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
users [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n`: Kullanıcı adlarını sadece bir kez gösterir, tekrar eden kullanıcı adlarını filtreler.
- `-r`: Sadece gerçek kullanıcıları gösterir, sistem kullanıcılarını hariç tutar.

## Yaygın Örnekler
Aşağıda `users` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Tüm aktif kullanıcıları listeleme:**

   ```bash
   users
   ```

2. **Tekrar eden kullanıcı adlarını filtreleme:**

   ```bash
   users -n
   ```

3. **Sadece gerçek kullanıcıları gösterme:**

   ```bash
   users -r
   ```

## İpuçları
- `users` komutunu, sistemdeki oturum açmış kullanıcıları hızlıca kontrol etmek için sıkça kullanabilirsiniz.
- Eğer birden fazla terminal açtıysanız, `users` komutunu kullanarak hangi kullanıcıların aktif olduğunu kolayca görebilirsiniz.
- Kullanıcıların hangi terminalde oturum açtığını görmek için `who` komutunu da kullanmayı düşünebilirsiniz.