# [Türkçe] Debian Almquist Shell (dash) pidstat Kullanımı: İşlem istatistiklerini görüntüleme

## Genel Bakış
`pidstat` komutu, sistemdeki işlemlerin performans istatistiklerini görüntülemek için kullanılır. Bu komut, belirli bir süre boyunca işlem başına CPU kullanımı, bellek kullanımı gibi bilgileri toplar ve kullanıcıya sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
pidstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Başlık satırını gösterir.
- `-r`: Bellek kullanımı istatistiklerini gösterir.
- `-u`: CPU kullanım istatistiklerini gösterir.
- `-p <PID>`: Belirli bir işlem kimliği (PID) için istatistikleri görüntüler.
- `-t`: İşlem alt süreçlerini de gösterir.

## Yaygın Örnekler
Aşağıda `pidstat` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm işlemler için CPU kullanımını gösterme:
   ```bash
   pidstat
   ```

2. Belirli bir işlem için (örneğin PID 1234) CPU ve bellek kullanımını görüntüleme:
   ```bash
   pidstat -r -u -p 1234
   ```

3. 2 saniye aralıklarla CPU kullanımını izleme:
   ```bash
   pidstat 2
   ```

4. Tüm işlemler için bellek kullanımını gösterme:
   ```bash
   pidstat -r
   ```

## İpuçları
- `pidstat` komutunu sık sık kullanıyorsanız, belirli bir PID'yi izlemek için bir alias oluşturmayı düşünebilirsiniz.
- Uzun süreli izlemeler için, çıktıyı bir dosyaya yönlendirmek faydalı olabilir:
  ```bash
  pidstat 2 > pidstat_output.txt
  ```
- Çıktıyı daha okunabilir hale getirmek için `grep` veya `awk` gibi diğer komutlarla birleştirebilirsiniz.