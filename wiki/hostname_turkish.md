# [Türkçe] Debian Almquist Shell (dash) hostname Kullanımı: [sistem adını görüntüleme ve ayarlama]

## Genel Bakış
`hostname` komutu, sistemin ağ üzerindeki adını görüntülemek veya ayarlamak için kullanılır. Bu komut, sistemin kimliğini belirlemek ve ağ üzerinde diğer cihazlarla iletişim kurmak için önemlidir.

## Kullanım
Komutun temel sözdizimi aşağıdaki gibidir:

```bash
hostname [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f`, `--fqdn`: Tam nitelikli alan adı (FQDN) olarak sistem adını gösterir.
- `-i`, `--ip-address`: Sistem adının IP adresini gösterir.
- `-s`, `--short`: Kısa sistem adını görüntüler.
- `--help`: Komut hakkında yardım bilgisi gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `hostname` komutunun bazı pratik kullanımları bulunmaktadır:

1. **Sistem adını görüntüleme:**
   ```bash
   hostname
   ```

2. **Tam nitelikli alan adı görüntüleme:**
   ```bash
   hostname -f
   ```

3. **Sistem adının IP adresini görüntüleme:**
   ```bash
   hostname -i
   ```

4. **Kısa sistem adını görüntüleme:**
   ```bash
   hostname -s
   ```

5. **Sistem adını değiştirme:**
   ```bash
   sudo hostname yeni-sistem-adi
   ```

## İpuçları
- Sistem adını değiştirdikten sonra, değişikliğin etkili olması için sistemi yeniden başlatmanız gerekebilir.
- Ağ ayarlarınıza uygun bir sistem adı seçmek, ağ üzerindeki diğer cihazlarla uyumluluğu artırır.
- `hostname` komutunu sık sık kullanarak sisteminizin adını ve durumunu kontrol etmek, ağ yönetimi için faydalı olabilir.