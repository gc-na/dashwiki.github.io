# [Türkçe] Debian Almquist Shell (dash) df Kullanımı: Disk alanı kullanımını gösterir

## Genel Bakış
`df` komutu, sistemdeki dosya sistemlerinin disk alanı kullanımını gösterir. Bu komut, her bir dosya sisteminin toplam, kullanılan ve boş alan miktarını görüntüleyerek kullanıcıların disk alanlarını yönetmelerine yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
df [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: İnsan tarafından okunabilir formatta çıktı verir (örneğin, KB, MB, GB).
- `-T`: Dosya sisteminin türünü gösterir.
- `-a`: Tüm dosya sistemlerini, boş olanlar dahil, gösterir.
- `-i`: İnode kullanımını gösterir.

## Yaygın Örnekler
Aşağıda `df` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm dosya sistemlerinin disk alanı kullanımını gösterme:
   ```bash
   df
   ```

2. İnsan tarafından okunabilir formatta disk alanı kullanımını gösterme:
   ```bash
   df -h
   ```

3. Belirli bir dosya sisteminin disk alanı kullanımını gösterme:
   ```bash
   df /dev/sda1
   ```

4. Dosya sisteminin türünü gösterme:
   ```bash
   df -T
   ```

5. İnode kullanımını gösterme:
   ```bash
   df -i
   ```

## İpuçları
- `df -h` seçeneğini kullanarak çıktıyı daha anlaşılır hale getirebilirsiniz.
- Disk alanı kullanımını düzenli olarak kontrol etmek, sistem yönetimi için iyi bir uygulamadır.
- Eğer belirli bir dosya sisteminin durumunu takip etmek istiyorsanız, `watch df -h` komutunu kullanarak sürekli güncellenen bir görünüm elde edebilirsiniz.