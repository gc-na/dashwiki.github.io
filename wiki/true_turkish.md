# [Türkçe] Debian Almquist Shell (dash) true Kullanımı: Her zaman başarılı bir çıkış sağlar

## Overview
`true` komutu, her zaman başarılı bir çıkış durumu döndüren bir komuttur. Genellikle, bir komutun başarılı bir şekilde çalıştığını belirtmek için veya bir komut dizisi içinde yer tutucu olarak kullanılır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
true [options] [arguments]
```

## Common Options
`true` komutunun herhangi bir özel seçeneği yoktur. Komut, yalnızca başarılı bir çıkış durumu döndürmek için tasarlanmıştır.

## Common Examples
Aşağıda `true` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Basit Kullanım:**
   ```bash
   true
   ```
   Bu komut, her zaman başarılı bir çıkış durumu (0) döndürür.

2. **Bir Komut Dizisinde Kullanım:**
   ```bash
   if true; then
       echo "Bu her zaman çalışır."
   fi
   ```
   Bu örnekte, `true` komutu her zaman başarılı olduğu için "Bu her zaman çalışır." mesajı ekrana yazdırılır.

3. **Bir Shell Script İçinde Kullanım:**
   ```bash
   #!/bin/dash
   true
   echo "Script başarıyla çalıştı."
   ```
   Bu script, `true` komutunu çalıştırdıktan sonra "Script başarıyla çalıştı." mesajını yazdırır.

## Tips
- `true` komutunu, bir komut dizisinde yer tutucu olarak kullanarak, belirli koşullar altında komutların çalışmasını kontrol edebilirsiniz.
- Hata ayıklama sırasında, bir komutun başarısız olmasını istemiyorsanız `true` komutunu kullanarak akışı devam ettirebilirsiniz.
- `true` komutunu, test senaryolarında veya otomasyon scriptlerinde kullanarak, belirli durumları simüle edebilirsiniz.