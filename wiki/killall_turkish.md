# [Türkçe] Debian Almquist Shell (dash) killall Kullanımı: Birden fazla işlemi sonlandırma

## Genel Bakış
`killall` komutu, belirtilen isimdeki tüm işlemleri sonlandırmak için kullanılır. Bu, belirli bir uygulamanın veya işlemin tüm örneklerini kapatmak istediğinizde oldukça yararlıdır.

## Kullanım
`killall` komutunun temel sözdizimi aşağıdaki gibidir:

```bash
killall [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u, --user <kullanıcı>`: Belirtilen kullanıcıya ait işlemleri sonlandırır.
- `-q, --quiet`: Hata mesajlarını bastırır.
- `-I, --ignore-case`: İşlem adında büyük/küçük harf duyarlılığını yok sayar.
- `-s, --signal <sinyal>`: Belirtilen sinyali gönderir (varsayılan olarak TERM sinyali gönderilir).

## Yaygın Örnekler
Aşağıda `killall` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Tüm `firefox` işlemlerini sonlandırma:**
   ```bash
   killall firefox
   ```

2. **Tüm `python` işlemlerini sonlandırma:**
   ```bash
   killall python
   ```

3. **Belirli bir kullanıcıya ait `ssh` işlemlerini sonlandırma:**
   ```bash
   killall -u kullanıcı_adı ssh
   ```

4. **Büyük/küçük harf duyarlılığını yok sayarak `chrome` işlemlerini sonlandırma:**
   ```bash
   killall -I chrome
   ```

5. **Özel bir sinyal göndererek `my_process` işlemini sonlandırma:**
   ```bash
   killall -s SIGKILL my_process
   ```

## İpuçları
- `killall` komutunu kullanmadan önce hangi işlemleri sonlandırmak istediğinizi dikkatlice kontrol edin; yanlışlıkla önemli bir işlemi kapatabilirsiniz.
- `-q` seçeneğini kullanarak gereksiz hata mesajlarını engelleyebilirsiniz, bu da komutunuzu daha temiz hale getirir.
- İşlemlerinizi yönetmek için `ps` veya `pgrep` gibi diğer komutlarla birlikte kullanmak, hangi işlemlerin çalıştığını görmek açısından faydalı olabilir.