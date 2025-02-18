# [Türkçe] Debian Almquist Shell (dash) getopts Kullanımı: Komut satırı argümanlarını işlemek için bir yöntem

## Genel Bakış
`getopts`, komut satırı argümanlarını işlemek için kullanılan bir komuttur. Özellikle betikler içinde, kullanıcıdan gelen seçenekleri ve argümanları düzenli bir şekilde almak için kullanılır. Bu, betiklerinizin daha esnek ve kullanıcı dostu olmasına yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```sh
getopts [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Seçenekleri topluca işlemek için kullanılır.
- `-b`: Belirli bir seçenek için bir argüman bekler.
- `-c`: Seçeneklerin sayısını sayar.
- `-d`: Varsayılan değerleri ayarlamak için kullanılır.

## Yaygın Örnekler
Aşağıda `getopts` komutunun bazı pratik örnekleri verilmiştir:

### Örnek 1: Basit Seçenek İşleme
```sh
#!/bin/sh
while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Seçenek A seçildi"
      ;;
    b)
      echo "Seçenek B ile argüman: $OPTARG"
      ;;
    c)
      echo "Seçenek C ile argüman: $OPTARG"
      ;;
    *)
      echo "Geçersiz seçenek"
      ;;
  esac
done
```

### Örnek 2: Çoklu Seçenekler
```sh
#!/bin/sh
while getopts "xyz" opt; do
  case $opt in
    x)
      echo "Seçenek X seçildi"
      ;;
    y)
      echo "Seçenek Y seçildi"
      ;;
    z)
      echo "Seçenek Z seçildi"
      ;;
    *)
      echo "Geçersiz seçenek"
      ;;
  esac
done
```

### Örnek 3: Argümanlı Seçenekler
```sh
#!/bin/sh
while getopts "f:n:" opt; do
  case $opt in
    f)
      echo "Dosya adı: $OPTARG"
      ;;
    n)
      echo "Numara: $OPTARG"
      ;;
    *)
      echo "Geçersiz seçenek"
      ;;
  esac
done
```

## İpuçları
- `getopts` kullanırken, seçeneklerinizi ve argümanlarınızı açık bir şekilde tanımlayın.
- Hatalı girişleri yönetmek için `*)` durumu eklemeyi unutmayın.
- Kullanıcı dostu bir deneyim sağlamak için, seçeneklerin ne işe yaradığını açıklayan bir yardım mesajı eklemeyi düşünün.