# [Türkçe] Debian Almquist Shell (dash) env Kullanımı: Ortam değişkenlerini görüntüleme ve ayarlama

## Genel Bakış
`env` komutu, ortam değişkenlerini görüntülemek veya yeni bir ortamda bir komut çalıştırmak için kullanılır. Bu komut, mevcut ortam değişkenlerini listeleyebilir veya belirli bir ortam değişkeni ayarlayarak bir komutu çalıştırmanıza olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
env [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Yeni bir ortam oluşturur, mevcut ortam değişkenlerini atlar.
- `-u`: Belirtilen ortam değişkenini kaldırır.
- `VAR=değer`: Belirli bir ortam değişkenini ayarlayarak bir komut çalıştırır.

## Yaygın Örnekler
Aşağıda `env` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Mevcut ortam değişkenlerini görüntüleme:**
   ```bash
   env
   ```

2. **Belirli bir ortam değişkenini ayarlayarak bir komut çalıştırma:**
   ```bash
   env MY_VAR=hello bash -c 'echo $MY_VAR'
   ```

3. **Bir ortam değişkenini kaldırarak bir komut çalıştırma:**
   ```bash
   env -u MY_VAR bash -c 'echo $MY_VAR'
   ```

4. **Yeni bir ortamda bir komut çalıştırma:**
   ```bash
   env -i bash -c 'printenv'
   ```

## İpuçları
- `env` komutunu, bir komutun hangi ortam değişkenleri ile çalıştığını test etmek için kullanabilirsiniz.
- Ortam değişkenlerini ayarlarken, değişken adlarının büyük harfle yazılmasına dikkat edin; küçük harfli değişkenler genellikle yerel değişkenlerdir.
- `env` komutunu, betiklerinizde belirli bir ortamda çalıştırmak istediğiniz komutlar için kullanarak daha taşınabilir hale getirebilirsiniz.