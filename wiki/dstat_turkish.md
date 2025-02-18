# [Türkçe] Debian Almquist Shell (dash) dstat Kullanımı: Sistem kaynaklarını izlemek için bir araç

## Genel Bakış
dstat, sistem kaynaklarını gerçek zamanlı olarak izlemek için kullanılan bir komut satırı aracıdır. CPU, bellek, disk ve ağ gibi sistem bileşenlerinin performansını takip etmenizi sağlar. Bu sayede sistem yöneticileri ve geliştiriciler, sistemin durumunu daha iyi anlayabilir ve gerektiğinde müdahale edebilir.

## Kullanım
dstat komutunun temel sözdizimi aşağıdaki gibidir:

```bash
dstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c`: CPU kullanımını gösterir.
- `-d`: Disk I/O istatistiklerini gösterir.
- `-n`: Ağ trafiğini gösterir.
- `-m`: Bellek kullanımını gösterir.
- `-t`: Zaman damgası ekler.

## Yaygın Örnekler
Aşağıda dstat komutunun bazı pratik örnekleri bulunmaktadır:

1. Sadece CPU kullanımını görüntülemek için:
   ```bash
   dstat -c
   ```

2. Disk I/O ve ağ trafiğini izlemek için:
   ```bash
   dstat -d -n
   ```

3. Tüm sistem kaynaklarını izlemek için:
   ```bash
   dstat
   ```

4. Zaman damgası ile birlikte bellek ve CPU kullanımını izlemek için:
   ```bash
   dstat -c -m -t
   ```

## İpuçları
- dstat'ı arka planda çalıştırarak sistemin durumunu sürekli izleyebilirsiniz. Bunu yapmak için `&` işaretini kullanabilirsiniz:
  ```bash
  dstat & 
  ```

- Çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  dstat > dstat_output.txt
  ```

- dstat'ı belirli bir süreyle sınırlamak için `--time` seçeneğini kullanabilirsiniz:
  ```bash
  dstat --time 10
  ```

Bu ipuçları ve örnekler, dstat komutunu etkili bir şekilde kullanmanıza yardımcı olacaktır.