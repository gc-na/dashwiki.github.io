# [Türkçe] Debian Almquist Shell (dash) ls Kullanımı: Dosya ve dizinleri listeleme

## Genel Bakış
`ls` komutu, bir dizindeki dosya ve dizinleri listelemek için kullanılır. Bu komut, kullanıcıların mevcut dizindeki içerikleri hızlıca görmesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```sh
ls [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Uzun formatta listeleme yapar, dosya izinleri, sahiplik bilgileri ve boyut gibi detayları gösterir.
- `-a`: Gizli dosyaları da dahil ederek tüm dosyaları listeler (nokta ile başlayan dosyalar).
- `-h`: Dosya boyutlarını insan tarafından okunabilir formatta gösterir (örneğin, K, M, G).
- `-R`: Alt dizinleri de dahil ederek, dizinleri rekürsif olarak listeler.
- `-t`: Dosyaları son değiştirilme tarihine göre sıralar.

## Yaygın Örnekler
Aşağıda `ls` komutunun bazı pratik örnekleri bulunmaktadır:

1. Temel dosya ve dizin listesini görüntüleme:
   ```sh
   ls
   ```

2. Gizli dosyaları da göstererek listeleme:
   ```sh
   ls -a
   ```

3. Uzun formatta detaylı listeleme:
   ```sh
   ls -l
   ```

4. İnsan tarafından okunabilir dosya boyutları ile listeleme:
   ```sh
   ls -lh
   ```

5. Alt dizinleri de içeren rekürsif listeleme:
   ```sh
   ls -R
   ```

6. Dosyaları son değiştirilme tarihine göre sıralayarak listeleme:
   ```sh
   ls -lt
   ```

## İpuçları
- `ls` komutunu kullanırken, seçenekleri birleştirerek daha fazla bilgi alabilirsiniz. Örneğin, `ls -la` komutu hem gizli dosyaları gösterir hem de uzun formatta listeleme yapar.
- Listeleme sonuçlarını daha iyi görmek için `less` komutuyla birleştirebilirsiniz: 
  ```sh
  ls -l | less
  ```
- Sık kullandığınız seçenekleri bir alias olarak tanımlayarak komutları daha hızlı yazabilirsiniz. Örneğin:
  ```sh
  alias ll='ls -l'
  ```