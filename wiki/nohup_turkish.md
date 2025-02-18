# [Türkçe] Debian Almquist Shell (dash) nohup Kullanımı: Arka planda komut çalıştırma

## Genel Bakış
`nohup` komutu, bir komutun terminal oturumu kapatılsa bile çalışmaya devam etmesini sağlar. Bu, uzun süren işlemleri başlatmak için oldukça kullanışlıdır; çünkü terminal kapandığında işlemin sonlanmasını engeller.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
nohup [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `&`: Komutu arka planda çalıştırmak için kullanılır.
- `-h`: Yardım bilgilerini gösterir.
- `-p`: Mevcut bir işlem için nohup kullanarak çalıştırır.

## Yaygın Örnekler
1. Basit bir komutun arka planda çalıştırılması:
   ```bash
   nohup sleep 100 &
   ```

2. Bir Python betiğinin arka planda çalıştırılması:
   ```bash
   nohup python3 my_script.py &
   ```

3. Çıktıyı bir dosyaya yönlendirme:
   ```bash
   nohup my_command > output.log &
   ```

4. Hata çıktısını ayrı bir dosyaya yönlendirme:
   ```bash
   nohup my_command > output.log 2> error.log &
   ```

## İpuçları
- `nohup` kullanırken çıktıyı bir dosyaya yönlendirmek, ileride hata ayıklama için faydalı olabilir.
- Komutun arka planda çalıştığından emin olmak için `jobs` komutunu kullanabilirsiniz.
- `disown` komutunu kullanarak, arka planda çalışan bir işlemi terminalden tamamen ayırabilirsiniz.