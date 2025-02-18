# [Türkçe] Debian Almquist Shell (dash) mv Kullanımı: Dosya ve dizin taşıma veya yeniden adlandırma

## Genel Bakış
`mv` komutu, dosyaları ve dizinleri taşımak veya yeniden adlandırmak için kullanılır. Bu komut, belirli bir dosyanın veya dizinin yerini değiştirmek veya ona yeni bir isim vermek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
mv [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Hedef dosya zaten varsa, üzerine yazmadan önce kullanıcıdan onay ister.
- `-u`: Sadece kaynak dosya, hedef dosyadan daha yeni ise taşır.
- `-v`: Taşıma işlemini ayrıntılı olarak gösterir; hangi dosyaların taşındığını belirtir.

## Yaygın Örnekler
Aşağıda `mv` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### Dosya Taşıma
Bir dosyayı başka bir dizine taşımak için:

```bash
mv dosya.txt /hedef/dizin/
```

### Dosya Yeniden Adlandırma
Bir dosyayı yeniden adlandırmak için:

```bash
mv eski_ad.txt yeni_ad.txt
```

### Dizin Taşıma
Bir dizini başka bir konuma taşımak için:

```bash
mv /kaynak/dizin/ /hedef/dizin/
```

### Kullanıcı Onayı ile Taşıma
Eğer hedef dosya varsa, kullanıcıdan onay almak için:

```bash
mv -i dosya.txt /hedef/dizin/
```

## İpuçları
- Dosyaları taşımadan önce, hedef dizinin var olduğundan emin olun.
- `-v` seçeneğini kullanarak hangi dosyaların taşındığını takip edebilirsiniz.
- Dosyaları taşımadan önce yedek almak, veri kaybını önlemek için iyi bir uygulamadır.