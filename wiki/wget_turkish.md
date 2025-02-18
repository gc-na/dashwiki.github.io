# [Türkçe] Debian Almquist Shell (dash) wget Kullanımı: Dosya indirme aracı

## Genel Bakış
`wget`, web üzerinden dosya indirmek için kullanılan güçlü bir komuttur. HTTP, HTTPS ve FTP protokollerini destekler ve kullanıcıların dosyaları kolayca indirmesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
wget [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-O [dosya_adı]`: İndirilen dosyayı belirtilen isimle kaydeder.
- `-c`: Kesilen bir indirmeyi devam ettirir.
- `-q`: Sessiz modda çalışır; yalnızca hata mesajlarını gösterir.
- `--limit-rate=[hız]`: İndirme hızını sınırlar.
- `-r`: Dizinleri ve alt dizinleri indirmek için rekürsif olarak çalışır.

## Yaygın Örnekler
Aşağıda `wget` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Basit bir dosya indirme:
   ```bash
   wget https://example.com/dosya.zip
   ```

2. İndirilen dosyayı farklı bir isimle kaydetme:
   ```bash
   wget -O yeni_dosya.zip https://example.com/dosya.zip
   ```

3. Kesilen bir indirmeyi devam ettirme:
   ```bash
   wget -c https://example.com/büyük_dosya.zip
   ```

4. İndirme hızını sınırlandırma:
   ```bash
   wget --limit-rate=200k https://example.com/dosya.zip
   ```

5. Rekürsif indirme:
   ```bash
   wget -r https://example.com/dizin/
   ```

## İpuçları
- İndirme işlemlerini daha verimli hale getirmek için `-q` seçeneğini kullanarak gereksiz çıktıları gizleyebilirsiniz.
- Büyük dosyalar indirirken `-c` seçeneği ile kesintisiz bir deneyim sağlayabilirsiniz.
- İndirme işlemlerini arka planda gerçekleştirmek için `nohup` komutunu kullanabilirsiniz. Örneğin:
  ```bash
  nohup wget https://example.com/büyük_dosya.zip &
  ```