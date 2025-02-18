# [Türkçe] Debian Almquist Shell (dash) umount Kullanımı: Dosya sistemlerini ayırma

## Genel Bakış
`umount` komutu, bağlı olan dosya sistemlerini ayırmak için kullanılır. Bu komut, bir dosya sisteminin artık kullanılmadığını belirtir ve sistem kaynaklarını serbest bırakır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
umount [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bağlı dosya sistemlerini ayırır.
- `-r`: Ayırma işlemi başarısız olursa dosya sistemini salt okunur olarak ayırmaya çalışır.
- `-f`: Zorla ayırma işlemi gerçekleştirir, bu seçenek genellikle dosya sistemi kullanılıyorsa kullanılır.
- `-l`: Geçici ayırma yapar; dosya sistemi, başka bir işlem tarafından kullanılmaya devam ediyorsa bile ayırma işlemi tamamlanır.

## Yaygın Örnekler
Aşağıda `umount` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir dosya sistemini ayırma:
   ```bash
   umount /mnt/usb
   ```

2. Tüm bağlı dosya sistemlerini ayırma:
   ```bash
   umount -a
   ```

3. Zorla bir dosya sistemini ayırma:
   ```bash
   umount -f /mnt/usb
   ```

4. Geçici ayırma işlemi:
   ```bash
   umount -l /mnt/usb
   ```

## İpuçları
- `umount` komutunu kullanmadan önce, ayırmak istediğiniz dosya sisteminin kullanılmadığından emin olun.
- Eğer bir dosya sistemi ayırılamıyorsa, `-f` seçeneğini kullanarak zorla ayırmayı deneyebilirsiniz.
- Ayırma işlemi sırasında hata alıyorsanız, ilgili dosya sisteminin açık dosyalarını kontrol edin ve kapatın.