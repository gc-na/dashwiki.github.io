# [Türkçe] Debian Almquist Shell (dash) at Kullanımı: Belirli bir zamanda komut çalıştırma

## Genel Bakış
`at` komutu, belirli bir zamanda bir komut veya betik çalıştırmak için kullanılır. Bu, zamanlanmış görevler oluşturmak için oldukça yararlıdır ve genellikle sistem yöneticileri tarafından otomatikleştirilmiş işlemler için tercih edilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
at [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f`: Belirtilen dosyadan komutları okur.
- `-m`: Komut çalıştırıldığında e-posta bildirimi gönderir.
- `-q`: Kuyruk tanımlayıcısını belirtir.
- `-l`: Planlanmış görevlerin listesini gösterir.
- `-d`: Belirli bir görevi iptal eder.

## Yaygın Örnekler
Aşağıda `at` komutunun bazı pratik örnekleri verilmiştir:

1. **Belirli bir zamanda komut çalıştırma:**
   ```bash
   echo "echo 'Merhaba Dünya'" | at 15:00
   ```

2. **Bir dosyadan komut çalıştırma:**
   ```bash
   at -f /path/to/script.sh 09:00
   ```

3. **E-posta bildirimi ile komut çalıştırma:**
   ```bash
   echo "backup.sh" | at -m 02:00
   ```

4. **Planlanmış görevlerin listesini görüntüleme:**
   ```bash
   at -l
   ```

5. **Belirli bir görevi iptal etme:**
   ```bash
   at -d 5
   ```

## İpuçları
- `at` komutunu kullanmadan önce, zaman formatını doğru girdiğinizden emin olun; saat dilimlerini göz önünde bulundurun.
- Uzun süreli görevler için, komutların doğru çalıştığından emin olmak için e-posta bildirimlerini kullanın.
- Planlanmış görevlerinizi düzenli olarak kontrol edin, böylece gereksiz görevleri iptal edebilirsiniz.