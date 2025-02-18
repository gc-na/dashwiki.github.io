# [Türkçe] Debian Almquist Shell (dash) telnet Kullanımı: Uzak bir sunucuya bağlantı kurma

## Genel Bakış
`telnet` komutu, kullanıcıların uzak bir sunucuya veya cihaza bağlantı kurmasını sağlayan bir ağ protokolüdür. Genellikle, uzak sistemlerle etkileşimde bulunmak için kullanılır ve metin tabanlı bir arayüz sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
telnet [seçenekler] [sunucu] [port]
```

## Yaygın Seçenekler
- `-l [kullanıcı]`: Belirtilen kullanıcı adı ile oturum açar.
- `-n [dosya]`: Belirtilen dosyaya bağlantı günlüğünü kaydeder.
- `-f [dosya]`: Belirtilen dosyadan bağlantı bilgilerini okur.

## Yaygın Örnekler
Aşağıda `telnet` komutunun bazı pratik kullanım örnekleri verilmiştir:

### 1. Bir sunucuya bağlanma
```bash
telnet example.com 80
```
Bu komut, `example.com` adresindeki 80 numaralı porta bağlanır.

### 2. Belirli bir kullanıcı adı ile bağlanma
```bash
telnet -l kullanıcı example.com
```
Bu komut, `example.com` adresine belirtilen kullanıcı adı ile bağlanır.

### 3. Bağlantı günlüğü kaydetme
```bash
telnet -n bağlantı_günlüğü.txt example.com 23
```
Bu komut, `example.com` adresindeki 23 numaralı porta bağlanırken bağlantı günlüğünü `bağlantı_günlüğü.txt` dosyasına kaydeder.

## İpuçları
- `telnet` komutunu kullanırken, güvenlik açısından dikkatli olun; çünkü bağlantılar şifrelenmemiştir.
- Uzak sunucularla etkileşimde bulunurken, doğru port numarasını kullandığınızdan emin olun.
- `telnet` ile bağlantı kurduğunuzda, komutları doğrudan sunucuya yazabilirsiniz; bu nedenle, komutları doğru girdiğinizden emin olun.