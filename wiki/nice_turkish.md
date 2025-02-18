# [Türkçe] Debian Almquist Shell (dash) nice Kullanımı: İşlem önceliğini ayarlama

## Genel Bakış
`nice` komutu, bir işlemin sistemdeki önceliğini ayarlamak için kullanılır. Bu, işlemin CPU kaynaklarını ne kadar kullanacağını belirler. Daha düşük bir öncelik değeri, işlem daha az CPU zamanı alır, bu da diğer işlemlerin daha iyi performans göstermesine yardımcı olur.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
nice [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n, --adjustment <değer>`: İşlemin öncelik değerini ayarlamak için kullanılır. Varsayılan değer 10'dur.
- `-h, --help`: Yardım mesajını görüntüler.
- `-V, --version`: Versiyon bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `nice` komutunun bazı pratik örnekleri bulunmaktadır:

1. Varsayılan öncelikle bir işlem başlatma:
   ```bash
   nice my_script.sh
   ```

2. Önceliği 5 olarak ayarlayarak bir işlem başlatma:
   ```bash
   nice -n 5 my_script.sh
   ```

3. Önceliği -10 olarak ayarlayarak bir işlem başlatma (daha yüksek öncelik):
   ```bash
   nice -n -10 my_script.sh
   ```

4. Bir komutun mevcut önceliğini görüntüleme:
   ```bash
   ps -o pid,ni,comm
   ```

## İpuçları
- `nice` komutunu kullanırken, öncelik değerinin -20 ile 19 arasında olduğunu unutmayın. -20 en yüksek öncelik, 19 ise en düşük önceliktir.
- İşlemlerin önceliklerini ayarlamak, sistem kaynaklarının daha verimli kullanılmasına yardımcı olabilir, bu nedenle yoğun kaynak kullanan işlemler için daha düşük öncelikler tercih edilebilir.
- `renice` komutunu kullanarak çalışan bir işlemin önceliğini değiştirebilirsiniz.