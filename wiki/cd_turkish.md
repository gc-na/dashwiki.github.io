# [Türkçe] Debian Almquist Shell (dash) cd Kullanımı: Dizinler arasında geçiş yapma komutu

## Genel Bakış
`cd` komutu, kullanıcıların dosya sisteminde dizinler arasında geçiş yapmalarını sağlar. Bu komut, terminalde çalışırken hangi dizinde olduğunuzu değiştirmek için kullanılır.

## Kullanım
`cd` komutunun temel sözdizimi aşağıdaki gibidir:

```bash
cd [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `..`: Bir üst dizine geçiş yapar.
- `-`: Önceki dizine geri döner.
- `~`: Kullanıcının ana dizinine geçiş yapar.

## Yaygın Örnekler
Aşağıda `cd` komutunun bazı pratik örnekleri bulunmaktadır:

1. Bir üst dizine geçiş yapmak için:
   ```bash
   cd ..
   ```

2. Önceki dizine geri dönmek için:
   ```bash
   cd -
   ```

3. Kullanıcının ana dizinine geçiş yapmak için:
   ```bash
   cd ~
   ```

4. Belirli bir dizine geçiş yapmak için:
   ```bash
   cd /home/kullanici/dizin
   ```

5. Göreceli bir yol kullanarak geçiş yapmak için:
   ```bash
   cd dizin1/dizin2
   ```

## İpuçları
- Dizin adlarını yazarken büyük/küçük harf duyarlılığına dikkat edin; Linux dosya sistemleri genellikle büyük/küçük harf duyarlıdır.
- Geçiş yapmak istediğiniz dizinin doğru yolunu bildiğinizden emin olun; yanlış bir yol hatalara neden olabilir.
- `pwd` komutunu kullanarak mevcut dizininizi kontrol edebilirsiniz.