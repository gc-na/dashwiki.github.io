# [Türkçe] Debian Almquist Shell (dash) umask Kullanımı: Dosya izinlerini ayarlama

## Overview
`umask` komutu, yeni oluşturulan dosya ve dizinlerin varsayılan izinlerini ayarlamak için kullanılır. Bu komut, kullanıcıların dosya ve dizinlerin erişim izinlerini kontrol etmelerine olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
umask [seçenekler] [argümanlar]
```

## Common Options
- `-S`: Umask değerini sembolik olarak gösterir.
- `-p`: Mevcut umask değerini gösterir.

## Common Examples
1. Mevcut umask değerini kontrol etmek için:
   ```bash
   umask
   ```

2. Umask değerini 022 olarak ayarlamak için:
   ```bash
   umask 022
   ```

3. Sembolik umask değerini görüntülemek için:
   ```bash
   umask -S
   ```

4. Umask değerini 0077 olarak ayarlamak için:
   ```bash
   umask 0077
   ```

## Tips
- Umask değerini ayarlarken, izinlerin hangi kullanıcı gruplarını etkilediğini göz önünde bulundurun.
- Umask ayarlarını, kullanıcı profil dosyalarınıza (örneğin, `.bashrc` veya `.profile`) ekleyerek her oturumda otomatik olarak uygulanmasını sağlayabilirsiniz.
- Geliştirme ortamlarında, dosya izinlerini dikkatlice ayarlamak, güvenlik açısından önemlidir.