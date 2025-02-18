# [Türkçe] Debian Almquist Shell (dash) jobs Kullanımı: Arka planda çalışan işlemleri listeleme

## Genel Bakış
`jobs` komutu, arka planda çalışan işlemleri listelemek için kullanılır. Bu komut, kullanıcıya terminalde başlatılan ve hala çalışmakta olan işlemleri gösterir. İşlemlerin durumunu ve kimlik numaralarını (PID) görüntüleyerek, kullanıcıların işlemleri yönetmesine yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
jobs [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: İşlemlerin PID'lerini de gösterir.
- `-n`: Sadece durumu değişen işlemleri gösterir.
- `-p`: Sadece işlemlerin PID'lerini gösterir.

## Yaygın Örnekler
Aşağıda `jobs` komutunun bazı pratik kullanımları verilmiştir:

1. Arka planda çalışan tüm işlemleri listeleme:
   ```bash
   jobs
   ```

2. PID'leri ile birlikte işlemleri listeleme:
   ```bash
   jobs -l
   ```

3. Sadece durumu değişen işlemleri gösterme:
   ```bash
   jobs -n
   ```

4. Sadece işlemlerin PID'lerini gösterme:
   ```bash
   jobs -p
   ```

## İpuçları
- `jobs` komutunu kullanarak, arka planda çalışan işlemleri takip edebilir ve gerektiğinde durdurabilir veya devam ettirebilirsiniz.
- İşlemleri yönetmek için `fg` (ön plana alma) veya `bg` (arka planda çalıştırma) komutları ile birlikte kullanabilirsiniz.
- İşlemlerin durumunu kontrol etmek, sistem kaynaklarını daha verimli kullanmanıza yardımcı olur.