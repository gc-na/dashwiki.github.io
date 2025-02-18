# [Türkçe] Debian Almquist Shell (dash) dig Kullanımı: DNS sorgulama aracı

## Genel Bakış
`dig` (Domain Information Groper), DNS (Domain Name System) sorguları yapmak için kullanılan bir komut satırı aracıdır. Bu komut, belirli bir alan adı hakkında bilgi almak için DNS sunucularına sorgular gönderir ve sonuçları kullanıcıya sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
dig [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `@sunucu`: Sorgunun gönderileceği DNS sunucusunu belirtir.
- `-t tip`: Sorgulamak istediğiniz kayıt türünü belirtir (örneğin, A, MX, CNAME).
- `+short`: Sonuçları daha kısa ve öz bir formatta gösterir.
- `+trace`: Sorgunun adım adım nasıl işlendiğini gösterir.

## Yaygın Örnekler
Aşağıda `dig` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Temel Alan Adı Sorgulama
```
dig example.com
```

### 2. Belirli Bir DNS Sunucusuna Sorgu Gönderme
```
dig @8.8.8.8 example.com
```

### 3. MX Kayıtlarını Sorgulama
```
dig -t MX example.com
```

### 4. Kısa Formatda Sonuç Alma
```
dig +short example.com
```

### 5. Sorgu İzleme
```
dig +trace example.com
```

## İpuçları
- `dig` komutunu kullanarak DNS sorunlarını teşhis etmek için farklı kayıt türlerini sorgulayabilirsiniz.
- Sık kullanılan DNS sunucularını (örneğin, Google DNS: 8.8.8.8) belirterek daha hızlı sonuçlar alabilirsiniz.
- Sonuçları daha iyi anlamak için `+short` seçeneğini kullanarak gereksiz bilgileri azaltabilirsiniz.