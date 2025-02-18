# [Türkçe] Debian Almquist Shell (dash) dirname Kullanımı: Dosya yolunu dizin adı olarak döndürme

## Genel Bakış
`dirname` komutu, bir dosya yolunu alarak, o dosyanın bulunduğu dizinin adını döndürür. Bu, dosya yollarını işlemek ve dizin yapısını anlamak için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:
```
dirname [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-z`: Boş dizin adlarını sıfır uzunlukta bir dize olarak döndürür.
- `--help`: Komutun kullanımını ve seçeneklerini gösterir.
- `--version`: Komutun sürüm bilgisini gösterir.

## Yaygın Örnekler
Aşağıda `dirname` komutunun bazı pratik örnekleri bulunmaktadır:

1. Basit bir dosya yolu için dizin adını almak:
   ```sh
   dirname /home/kullanici/dosya.txt
   ```
   Çıktı:
   ```
   /home/kullanici
   ```

2. Bir dizin yolunu kullanarak dizin adını almak:
   ```sh
   dirname /var/log/syslog
   ```
   Çıktı:
   ```
   /var/log
   ```

3. Boş bir dizin adı ile kullanmak:
   ```sh
   dirname /home/kullanici/
   ```
   Çıktı:
   ```
   /home/kullanici
   ```

4. Birden fazla dosya yolu için dizin adlarını almak:
   ```sh
   dirname /usr/local/bin/script.sh /etc/hosts
   ```
   Çıktı:
   ```
   /usr/local/bin
   /etc
   ```

## İpuçları
- `dirname` komutunu, dosya yollarını işleyen betikler yazarken kullanmak, kodunuzu daha okunabilir hale getirebilir.
- Dizin adlarını almak için `basename` komutuyla birlikte kullanarak dosya adlarını ve dizin adlarını ayrı ayrı elde edebilirsiniz.
- Uzun dosya yollarını işlerken, `dirname` komutunu bir değişkene atayarak daha sonra kullanabilirsiniz. Örneğin:
   ```sh
   dizin=$(dirname /path/to/your/file.txt)
   echo "Dizin: $dizin"
   ```