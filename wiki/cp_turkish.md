# [Türkçe] Debian Almquist Shell (dash) cp Kullanımı: Dosyaları kopyalama

## Genel Bakış
`cp` komutu, dosyaları ve dizinleri bir yerden başka bir yere kopyalamak için kullanılır. Bu komut, kullanıcıların dosyalarını yedeklemek veya düzenlemek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:
```
cp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-r`: Dizinleri ve içindeki dosyaları kopyalamak için kullanılır (rekürsif).
- `-i`: Hedef dosya mevcutsa kullanıcıdan onay ister.
- `-u`: Sadece kaynak dosya hedef dosyadan daha yeni ise kopyalar.
- `-v`: Kopyalama işlemi sırasında hangi dosyaların kopyalandığını gösterir (ayrıntılı çıktı).

## Yaygın Örnekler
1. Basit bir dosya kopyalama:
   ```bash
   cp dosya.txt yedek_dosya.txt
   ```

2. Bir dizini ve içindeki dosyaları kopyalama:
   ```bash
   cp -r kaynak_dizin/ hedef_dizin/
   ```

3. Kullanıcı onayı ile dosya kopyalama:
   ```bash
   cp -i dosya.txt yedek_dosya.txt
   ```

4. Sadece daha yeni dosyaları kopyalama:
   ```bash
   cp -u dosya.txt yedek_dosya.txt
   ```

5. Kopyalama işlemi sırasında ayrıntılı bilgi görüntüleme:
   ```bash
   cp -v dosya.txt yedek_dosya.txt
   ```

## İpuçları
- Kopyalama işlemi yapmadan önce, hedef dizinin var olup olmadığını kontrol edin.
- `-i` seçeneğini kullanarak yanlışlıkla üzerine yazma riskini azaltabilirsiniz.
- Büyük dosyaları kopyalarken, `-v` seçeneği ile işlemin ilerleyişini takip edebilirsiniz.