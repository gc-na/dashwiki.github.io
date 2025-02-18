# [Türkçe] Debian Almquist Shell (dash) socat Kullanımı: İletişim kanalları arasında veri aktarımı

## Genel Bakış
`socat`, iki veri akışı arasında veri aktarımı sağlayan bir komut satırı aracıdır. Bu araç, ağ bağlantıları, dosyalar veya diğer veri kaynakları arasında köprü kurarak veri iletimini kolaylaştırır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
socat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u`: Verileri yalnızca bir yönde iletmek için kullanılır.
- `-v`: Ayrıntılı çıktı sağlar, bu sayede işlem sırasında neler olduğunu görebilirsiniz.
- `TCP:<host>:<port>`: Belirtilen IP adresine ve porta TCP bağlantısı kurar.
- `UDP:<host>:<port>`: Belirtilen IP adresine ve porta UDP bağlantısı kurar.
- `FILE:<dosya_adı>`: Belirtilen dosyayı veri akışı olarak kullanır.

## Yaygın Örnekler
Aşağıda `socat` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Yerel bir TCP sunucusu oluşturma:**
   ```bash
   socat TCP-LISTEN:1234,fork EXEC:/bin/cat
   ```
   Bu komut, 1234 numaralı portta dinleyen bir TCP sunucusu oluşturur ve gelen verileri `cat` komutuna yönlendirir.

2. **Bir dosyadan veri okuma ve TCP bağlantısına gönderme:**
   ```bash
   socat FILE:/path/to/file TCP:localhost:1234
   ```
   Bu komut, belirtilen dosyadan veri okur ve bunu localhost'taki 1234 numaralı porta gönderir.

3. **İki TCP bağlantısını birbirine bağlama:**
   ```bash
   socat TCP:server1:1234 TCP:server2:5678
   ```
   Bu komut, `server1` üzerindeki 1234 numaralı port ile `server2` üzerindeki 5678 numaralı port arasında bir köprü kurar.

## İpuçları
- `socat` kullanırken, bağlantıların doğru bir şekilde kurulduğundan emin olun. Hatalı bağlantılar veri kaybına neden olabilir.
- Ayrıntılı hata ayıklama için `-v` seçeneğini kullanarak işleminiz hakkında daha fazla bilgi edinebilirsiniz.
- Güvenlik açısından, ağ üzerinden veri aktarırken şifreleme yöntemlerini (örneğin, SSL/TLS) kullanmayı düşünün.