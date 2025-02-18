# [Türkçe] Debian Almquist Shell (dash) netcat Kullanımı: Ağ bağlantıları ve veri aktarımı

## Genel Bakış
Netcat, ağ bağlantıları kurmak ve veri aktarmak için kullanılan güçlü bir araçtır. TCP ve UDP protokollerini destekler ve genellikle ağ sorunlarını gidermek, veri transferi yapmak veya basit bir sunucu/istemci uygulaması oluşturmak için kullanılır.

## Kullanım
Netcat komutunun temel sözdizimi aşağıdaki gibidir:

```bash
netcat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Dinleme modunu etkinleştirir, yani gelen bağlantıları kabul eder.
- `-p`: Dinleme portunu belirtir.
- `-u`: UDP protokolünü kullanır.
- `-v`: Ayrıntılı modda çalışır, daha fazla bilgi verir.
- `-z`: Sadece bağlantı testi yapar, veri göndermez.

## Yaygın Örnekler
1. **Basit bir TCP sunucusu oluşturma:**
   ```bash
   netcat -l -p 1234
   ```
   Bu komut, 1234 numaralı portta dinleyen bir TCP sunucusu oluşturur.

2. **Bir istemciden sunucuya veri gönderme:**
   ```bash
   echo "Merhaba, dünya!" | netcat localhost 1234
   ```
   Bu komut, "Merhaba, dünya!" mesajını localhost üzerindeki 1234 numaralı portta dinleyen sunucuya gönderir.

3. **UDP üzerinden veri gönderme:**
   ```bash
   echo "UDP mesajı" | netcat -u localhost 1234
   ```
   Bu komut, UDP protokolü kullanarak "UDP mesajı" gönderir.

4. **Bir dosyayı başka bir makineye gönderme:**
   ```bash
   netcat -l -p 1234 > gelen_dosya.txt
   ```
   Başka bir terminalde:
   ```bash
   netcat [hedef_ip] 1234 < gonderilecek_dosya.txt
   ```
   Bu komut, `gonderilecek_dosya.txt` dosyasını belirtilen IP adresine gönderir.

## İpuçları
- Netcat kullanırken güvenlik önlemlerini göz önünde bulundurun; açık portlar kötü niyetli kullanıcılar tarafından kullanılabilir.
- Dinleme modunda çalışırken, yalnızca güvenilir kaynaklardan gelen bağlantılara izin vermek için firewall ayarlarını kontrol edin.
- Netcat'i bir ağ testi aracı olarak kullanırken, `-v` seçeneği ile daha fazla bilgi alabilirsiniz.