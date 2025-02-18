# [Türkçe] Debian Almquist Shell (dash) free komutu: Bellek kullanımını görüntüleme

## Genel Bakış
`free` komutu, sistemdeki bellek kullanımını gösterir. RAM ve takas bellek (swap) alanlarının ne kadarının kullanıldığını ve ne kadarının boş olduğunu hızlı bir şekilde görüntülemenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
free [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: İnsan tarafından okunabilir formatta çıktı verir (örneğin, KB, MB, GB).
- `-m`: Çıktıyı megabayt cinsinden gösterir.
- `-g`: Çıktıyı gigabayt cinsinden gösterir.
- `-s [saniye]`: Belirtilen saniye aralıklarıyla sürekli güncellenen bir çıktı sağlar.
- `-t`: Toplam bellek kullanımını gösterir.

## Yaygın Örnekler
Aşağıda `free` komutunun bazı pratik örnekleri verilmiştir:

1. Temel bellek bilgilerini görüntüleme:
   ```bash
   free
   ```

2. İnsan tarafından okunabilir formatta bellek bilgilerini görüntüleme:
   ```bash
   free -h
   ```

3. Bellek bilgilerini megabayt cinsinden görüntüleme:
   ```bash
   free -m
   ```

4. 5 saniye aralıklarla bellek bilgilerini güncelleme:
   ```bash
   free -s 5
   ```

5. Toplam bellek kullanımını gösterme:
   ```bash
   free -t
   ```

## İpuçları
- `free -h` kullanarak bellek kullanımını daha kolay anlamak için insan tarafından okunabilir formatta görüntüleyin.
- Bellek kullanımını izlemek için `free -s` seçeneğini kullanarak belirli aralıklarla güncellemeleri takip edebilirsiniz.
- Sistem performansını değerlendirmek için `free` komutunu diğer sistem izleme araçlarıyla birleştirin.