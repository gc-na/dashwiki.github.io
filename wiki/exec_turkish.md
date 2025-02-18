# [Türkçe] Debian Almquist Shell (dash) exec Kullanımı: Komutları yeni bir işlem olarak çalıştırma

## Genel Bakış
`exec` komutu, mevcut shell oturumunu yeni bir komutla değiştirmek için kullanılır. Bu, yeni bir işlem başlatmak yerine mevcut işlemi değiştirdiği için, mevcut shell'in yerini alan bir komut çalıştırır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```sh
exec [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a, --arg`: Yeni işlem için verilen argümanı kullanarak çalıştırır.
- `-l, --login`: Yeni işlemi bir giriş kabuğu olarak başlatır.
- `-c, --command`: Verilen komutu çalıştırır.

## Yaygın Örnekler
Aşağıda `exec` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Yeni bir shell başlatma
Mevcut shell'i `bash` ile değiştirmek için:

```sh
exec bash
```

### Örnek 2: Bir komut çalıştırma
Mevcut shell'i `ls` komutuyla değiştirmek için:

```sh
exec ls -l
```

### Örnek 3: Giriş shell'i olarak başlatma
Yeni bir shell oturumunu giriş shell'i olarak başlatmak için:

```sh
exec -l sh
```

## İpuçları
- `exec` komutunu kullanmadan önce, mevcut shell oturumunuzda kaydedilmesi gereken herhangi bir veri olup olmadığını kontrol edin, çünkü `exec` mevcut shell'i değiştirecektir.
- `exec` komutunu, betiklerinizi daha verimli hale getirmek için kullanabilirsiniz; bu sayede gereksiz alt işlemler oluşturulmaz.
- `exec` ile çalıştırdığınız komutun, shell oturumunuza geri dönmeyeceğini unutmayın; bu nedenle dikkatli kullanın.