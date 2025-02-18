# [Türkçe] Debian Almquist Shell (dash) basename Kullanımı: Dosya adını ayıklama

## Genel Bakış
`basename` komutu, bir dosya yolundan yalnızca dosya adını çıkarmak için kullanılır. Bu, dosya yolunun son kısmını alarak, dosyanın adını ve uzantısını izole etmenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
basename [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Birden fazla dosya adı için `basename` komutunu çalıştırır.
- `-s`: Belirtilen bir uzantıyı dosya adından kaldırır.

## Yaygın Örnekler
Aşağıda `basename` komutunun bazı pratik örnekleri bulunmaktadır:

1. Basit bir dosya adı ayıklama:
   ```bash
   basename /home/kullanici/dosya.txt
   ```
   Çıktı:
   ```
   dosya.txt
   ```

2. Uzantıyı kaldırarak dosya adını alma:
   ```bash
   basename /home/kullanici/dosya.txt .txt
   ```
   Çıktı:
   ```
   dosya
   ```

3. Birden fazla dosya adı için kullanma:
   ```bash
   basename -a /home/kullanici/dosya1.txt /home/kullanici/dosya2.txt
   ```
   Çıktı:
   ```
   dosya1.txt
   dosya2.txt
   ```

## İpuçları
- `basename` komutunu, dosya adlarını işlemek için betiklerde kullanabilirsiniz; bu, dosya adlarını dinamik olarak almak için faydalıdır.
- Uzantıları kaldırmak için `-s` seçeneğini kullanarak, dosya adlarını daha okunabilir hale getirebilirsiniz.
- Birden fazla dosya adı ile çalışırken, `-a` seçeneğini kullanarak tek bir komutla hepsini işleyebilirsiniz.