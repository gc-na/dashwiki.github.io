# [Türkçe] Debian Almquist Shell (dash) kill Kullanımı: Süreçleri sonlandırma komutu

## Genel Bakış
`kill` komutu, işletim sisteminde çalışan süreçleri sonlandırmak için kullanılır. Belirli bir süreç kimliğine (PID) sahip olan bir süreci durdurmak veya öldürmek için bu komut kullanılır.

## Kullanım
Komutun temel sözdizimi aşağıdaki gibidir:

```bash
kill [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Tüm sinyal isimlerini listele.
- `-s`: Göndermek istediğiniz sinyalin adını veya numarasını belirtin.
- `-n`: Sinyal numarasını belirtin.

## Yaygın Örnekler
Aşağıda `kill` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir PID ile süreci sonlandırma:
   ```bash
   kill 1234
   ```

2. Belirli bir sinyal göndererek süreci sonlandırma (örneğin, SIGKILL):
   ```bash
   kill -9 1234
   ```

3. Tüm süreçleri sonlandırmak için bir sinyal gönderme:
   ```bash
   killall -9 process_name
   ```

4. Belirli bir sinyal ile süreci durdurma (örneğin, SIGTERM):
   ```bash
   kill -15 1234
   ```

## İpuçları
- Süreçleri sonlandırmadan önce, hangi süreçlerin çalıştığını görmek için `ps` veya `top` komutlarını kullanabilirsiniz.
- `kill` komutunu kullanırken, yanlışlıkla önemli bir süreci sonlandırmamak için dikkatli olun.
- Süreçlerinizi yönetmek için `pkill` veya `killall` gibi diğer komutları da göz önünde bulundurabilirsiniz.