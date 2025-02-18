# [Türkçe] Debian Almquist Shell (dash) curl Kullanımı: Web'den veri almak için bir araç

## Genel Bakış
`curl`, URL'ler üzerinden veri transferi yapmak için kullanılan bir komut satırı aracıdır. HTTP, HTTPS, FTP ve daha birçok protokolü destekler. Genellikle web'den veri indirmek veya API'lerle etkileşimde bulunmak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
curl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-O`: İndirilen dosyayı, URL'deki dosya adıyla kaydeder.
- `-L`: Yönlendirmeleri takip eder.
- `-d`: POST isteği ile veri gönderir.
- `-H`: Özel başlıklar ekler.
- `-u`: Kullanıcı adı ve şifre ile kimlik doğrulaması yapar.

## Yaygın Örnekler
Aşağıda `curl` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Basit bir HTTP isteği
```
curl http://example.com
```
Bu komut, `example.com` adresine bir HTTP isteği gönderir ve yanıtı terminalde gösterir.

### 2. Dosya indirme
```
curl -O http://example.com/dosya.zip
```
Bu komut, `dosya.zip` dosyasını `example.com` adresinden indirir ve mevcut dizine kaydeder.

### 3. Yönlendirmeleri takip etme
```
curl -L http://example.com
```
Bu komut, `example.com` adresine yapılan bir isteği yönlendirmeleri takip ederek gerçekleştirir.

### 4. POST isteği ile veri gönderme
```
curl -d "param1=değer1&param2=değer2" http://example.com/api
```
Bu komut, belirtilen URL'ye POST isteği ile veri gönderir.

### 5. Özel başlık ekleme
```
curl -H "Authorization: Bearer TOKEN" http://example.com/api
```
Bu komut, bir API isteği yaparken özel bir yetkilendirme başlığı ekler.

## İpuçları
- `curl` komutunu daha verimli kullanmak için `-v` seçeneğini ekleyerek ayrıntılı çıktı alabilirsiniz.
- Sık kullandığınız `curl` komutlarını bir betik dosyasına kaydedip daha sonra çalıştırabilirsiniz.
- Güvenlik açısından, hassas verileri (şifreler gibi) komut satırında açıkça yazmaktan kaçının. Bunun yerine, `-u` seçeneği ile kullanıcı adı ve şifreyi girmeyi tercih edin.