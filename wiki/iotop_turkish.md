# [Türkçe] Debian Almquist Shell (dash) iotop Kullanımı: Disk I/O işlemlerini izleme aracı

## Genel Bakış
iotop, sistemdeki disk girdi/çıktı (I/O) işlemlerini izlemek için kullanılan bir komuttur. Bu komut, hangi süreçlerin disk üzerinde ne kadar veri okuduğunu veya yazdığını göstererek, sistem performansını analiz etmenize yardımcı olur.

## Kullanım
Temel komut yapısı aşağıdaki gibidir:

```bash
iotop [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-o`, `--only`: Sadece disk I/O işlemi yapan süreçleri gösterir.
- `-b`, `--batch`: Çıktıyı toplu modda gösterir, bu da komutun arka planda çalışmasına olanak tanır.
- `-d`, `--delay`: Çıktının güncellenme süresini ayarlar (varsayılan 1 saniyedir).
- `-p`, `--pid`: Belirli bir süreç kimliğine (PID) göre filtreleme yapar.

## Yaygın Örnekler
Aşağıda iotop komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Temel Kullanım:**
   Disk I/O işlemlerini izlemek için sadece `iotop` komutunu çalıştırabilirsiniz.
   ```bash
   iotop
   ```

2. **Sadece I/O yapan süreçleri gösterme:**
   Sadece disk I/O işlemi gerçekleştiren süreçleri görmek için `-o` seçeneğini kullanın.
   ```bash
   iotop -o
   ```

3. **Toplu Modda Çalıştırma:**
   Çıktıyı toplu modda almak için `-b` seçeneği ile birlikte bir dosyaya yönlendirebilirsiniz.
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. **Güncelleme Süresini Ayarlama:**
   Güncellemelerin her 2 saniyede bir yapılmasını istiyorsanız `-d` seçeneğini kullanın.
   ```bash
   iotop -d 2
   ```

5. **Belirli Bir PID için İzleme:**
   Belirli bir süreç kimliğine (PID) göre izleme yapmak için `-p` seçeneğini kullanın.
   ```bash
   iotop -p 1234
   ```

## İpuçları
- iotop komutunu çalıştırmak için genellikle root yetkilerine ihtiyaç duyarsınız. Bu nedenle `sudo` ile çalıştırmak gerekebilir.
- Uzun süreli izleme yapacaksanız, çıktıyı bir dosyaya yönlendirmek iyi bir fikir olabilir.
- Disk I/O sorunlarını analiz ederken, hangi süreçlerin en fazla kaynak tükettiğini belirlemek için `-o` seçeneğini kullanmak faydalıdır.