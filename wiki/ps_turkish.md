# [Türkçe] Debian Almquist Shell (dash) ps Kullanımı: Süreçleri görüntüleme

## Genel Bakış
`ps` komutu, sistemde çalışan süreçlerin listesini görüntülemek için kullanılır. Bu komut, kullanıcıların hangi işlemlerin çalıştığını ve bu işlemlerle ilgili bilgileri görmelerine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
ps [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Tüm süreçleri gösterir.
- `-f`: Tam formatta bilgi gösterir.
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait süreçleri listeler.
- `-p [PID]`: Belirtilen süreç kimliğine (PID) sahip süreci gösterir.
- `aux`: Tüm süreçleri detaylı bir şekilde gösterir.

## Yaygın Örnekler
Aşağıda `ps` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm süreçleri listeleme:
    ```bash
    ps -e
    ```

2. Belirli bir kullanıcıya ait süreçleri görüntüleme:
    ```bash
    ps -u kullanıcı_adı
    ```

3. Tam formatta süreç bilgilerini gösterme:
    ```bash
    ps -ef
    ```

4. Belirli bir süreç kimliğine sahip süreci görüntüleme:
    ```bash
    ps -p 1234
    ```

5. Tüm süreçleri detaylı bir şekilde gösterme:
    ```bash
    ps aux
    ```

## İpuçları
- `ps` komutunu `grep` ile birleştirerek belirli bir süreci kolayca bulabilirsiniz:
    ```bash
    ps aux | grep sürec_adı
    ```
- Süreçlerin daha iyi anlaşılması için `-f` seçeneğini kullanarak daha fazla bilgi edinebilirsiniz.
- Süreçlerin sürekli güncellenen bir listesini görmek için `top` komutunu kullanmayı düşünebilirsiniz.