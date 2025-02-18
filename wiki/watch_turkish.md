# [Türkçe] Debian Almquist Shell (dash) watch kullanımı: Komutları periyodik olarak çalıştırma

## Genel Bakış
`watch` komutu, belirli bir komutu belirli aralıklarla çalıştırarak çıktısını ekranda güncelleyerek gösterir. Bu, sistem durumunu izlemek veya sürekli değişen verileri takip etmek için oldukça yararlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
watch [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n, --interval <saniye>`: Komutun ne sıklıkla çalıştırılacağını belirler. Varsayılan olarak 2 saniyedir.
- `-d, --differences`: Çıktıdaki değişiklikleri vurgular.
- `-t, --no-title`: Başlık satırını gizler.
- `-x, --exec`: Komutun çalıştırılmasını sağlar ve çıktısını gösterir.

## Yaygın Örnekler
1. **Bir dizindeki dosyaları her 5 saniyede bir kontrol etme:**
   ```bash
   watch -n 5 ls -l
   ```

2. **Sistem kaynak kullanımını izleme:**
   ```bash
   watch -n 1 free -h
   ```

3. **Belirli bir dosyanın içeriğini izleme ve değişiklikleri vurgulama:**
   ```bash
   watch -d cat /var/log/syslog
   ```

4. **Bir ağ bağlantısının durumunu kontrol etme:**
   ```bash
   watch -n 10 ping -c 1 google.com
   ```

## İpuçları
- `-d` seçeneğini kullanarak, çıktınızdaki değişiklikleri daha kolay fark edebilirsiniz.
- Uzun süreli izlemelerde, `-t` seçeneği ile başlık satırını gizleyerek ekranınızı daha temiz tutabilirsiniz.
- İzlemek istediğiniz komutun çıktısını önceden test etmek, `watch` komutunu kullanmadan önce faydalı olabilir.