# [Türkçe] Debian Almquist Shell (dash) time kullanımı: Komutların çalışma süresini ölçme

## Genel Bakış
`time` komutu, bir komutun çalıştırılması için geçen süreyi ölçmek için kullanılır. Bu komut, özellikle performans analizi ve optimizasyon çalışmaları için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
time [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Daha basit bir çıktı formatı sağlar.
- `-o dosya`: Çıktıyı belirtilen dosyaya yönlendirir.
- `-v`: Daha ayrıntılı bir zamanlama raporu verir.

## Yaygın Örnekler
Aşağıda `time` komutunun bazı pratik örnekleri bulunmaktadır:

1. Basit bir komutun çalışma süresini ölçme:
   ```bash
   time sleep 2
   ```

2. Çıktıyı bir dosyaya yönlendirme:
   ```bash
   time -o zaman.txt ls -l
   ```

3. Daha ayrıntılı bir zamanlama raporu alma:
   ```bash
   time -v find / -name "dosya.txt"
   ```

4. Bir komutu zamanlayarak çalıştırma:
   ```bash
   time bash -c "for i in {1..100000}; do echo $i; done"
   ```

## İpuçları
- `time` komutunu, uzun süren işlemleri analiz etmek için kullanarak hangi komutların daha fazla zaman aldığını belirleyebilirsiniz.
- Çıktıyı dosyaya yönlendirmek, zamanlama sonuçlarını daha sonra incelemek için faydalıdır.
- `-v` seçeneği ile daha fazla bilgi almak, performans sorunlarını tespit etmenize yardımcı olabilir.