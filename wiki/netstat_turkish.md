# [Türkçe] Debian Almquist Shell (dash) netstat Kullanımı: Ağ bağlantılarını görüntüleme

## Genel Bakış
`netstat` komutu, ağ bağlantılarını, yönlendirme tablolarını ve ağ arayüzlerinin istatistiklerini görüntülemek için kullanılır. Bu komut, sistemdeki aktif ağ bağlantılarını ve bu bağlantılarla ilgili bilgileri hızlı bir şekilde analiz etmenizi sağlar.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
netstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bağlantıları ve dinleme portlarını gösterir.
- `-t`: TCP bağlantılarını gösterir.
- `-u`: UDP bağlantılarını gösterir.
- `-n`: Adresleri ve port numaralarını sayısal olarak gösterir.
- `-l`: Sadece dinleyen bağlantıları gösterir.
- `-p`: Bağlantıların hangi süreç tarafından kullanıldığını gösterir.

## Yaygın Örnekler
Aşağıda `netstat` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm aktif bağlantıları ve dinleme portlarını görüntüleme:
   ```bash
   netstat -a
   ```

2. Sadece TCP bağlantılarını listeleme:
   ```bash
   netstat -t
   ```

3. Sadece dinleyen bağlantıları gösterme:
   ```bash
   netstat -l
   ```

4. Bağlantıları sayısal formatta görüntüleme:
   ```bash
   netstat -n
   ```

5. Belirli bir süreçle ilişkili bağlantıları görüntüleme:
   ```bash
   netstat -p
   ```

## İpuçları
- `netstat` komutunu `grep` ile birleştirerek belirli bir bağlantıyı veya portu filtreleyebilirsiniz. Örneğin, 80 numaralı portu dinleyen bağlantıları bulmak için:
  ```bash
  netstat -tuln | grep ':80'
  ```

- Ağ sorunlarını teşhis etmek için `netstat` çıktısını düzenli olarak kontrol edin. Bu, beklenmeyen bağlantıları veya dinleyen portları tespit etmenize yardımcı olabilir.

- `netstat` komutunu kullanırken, sistemdeki ağ trafiğini anlamak için diğer ağ araçlarıyla birlikte kullanmayı düşünün. Örneğin, `ping` veya `traceroute` gibi komutlar, ağ bağlantılarının durumunu daha iyi anlamanızı sağlar.