# [Türkçe] Debian Almquist Shell (dash) id Kullanımı: Kullanıcı kimliğini gösterir

## Genel Bakış
`id` komutu, kullanıcı kimliğini ve grup bilgilerini görüntülemek için kullanılır. Bu komut, sistemdeki kullanıcıların kimlik bilgilerini hızlı bir şekilde kontrol etmenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
id [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u`: Kullanıcının UID'sini (Kullanıcı Kimliği) gösterir.
- `-g`: Kullanıcının GID'sini (Grup Kimliği) gösterir.
- `-G`: Kullanıcının ait olduğu tüm grup kimliklerini gösterir.
- `-n`: Kullanıcı adını veya grup adını gösterir.
- `-r`: Gerçek UID veya GID'yi gösterir.

## Yaygın Örnekler
Aşağıda `id` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Kullanıcı kimliğini görüntüleme:
   ```bash
   id
   ```

2. Belirli bir kullanıcının kimlik bilgilerini görüntüleme:
   ```bash
   id kullanıcı_adı
   ```

3. Kullanıcının UID'sini görüntüleme:
   ```bash
   id -u
   ```

4. Kullanıcının GID'sini görüntüleme:
   ```bash
   id -g
   ```

5. Kullanıcının ait olduğu grup kimliklerini görüntüleme:
   ```bash
   id -G
   ```

## İpuçları
- `id` komutunu kullanarak, sistemdeki kullanıcı ve grup bilgilerinizi hızlıca kontrol edebilirsiniz.
- Özellikle çok kullanıcılı sistemlerde, hangi gruplara ait olduğunuzu öğrenmek için `id -G` seçeneğini kullanmak faydalıdır.
- `id` komutunun çıktısını bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz. Örneğin:
  ```bash
  id > kullanici_bilgileri.txt
  ```