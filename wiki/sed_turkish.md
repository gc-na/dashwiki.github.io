# [Türkçe] Debian Almquist Shell (dash) sed Kullanımı: Metin düzenleme aracı

## Genel Bakış
`sed`, akış halinde metin düzenleme işlemleri gerçekleştiren bir komut satırı aracıdır. Genellikle dosyalar içindeki metinleri değiştirmek, silmek veya eklemek için kullanılır. `sed`, "stream editor" (akış düzenleyici) anlamına gelir ve metin akışını satır satır işleyerek düzenlemeler yapar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
sed [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Birden fazla komut belirtmek için kullanılır.
- `-i`: Dosya üzerinde doğrudan değişiklik yapar (yerinde düzenleme).
- `-n`: Varsayılan çıktıyı bastırır; yalnızca belirtilen komutlarla sonuçları gösterir.
- `s/pattern/replacement/`: Belirtilen deseni değiştirir.

## Yaygın Örnekler
Aşağıda `sed` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Basit Metin Değiştirme
Bir dosyadaki "eski" kelimesini "yeni" ile değiştirmek için:
```bash
sed 's/eski/yeni/' dosya.txt
```

### 2. Yerinde Değiştirme
Bir dosyadaki "eski" kelimesini "yeni" ile yerinde değiştirmek için:
```bash
sed -i 's/eski/yeni/g' dosya.txt
```

### 3. Belirli Satırları Gösterme
Sadece 2. satırı göstermek için:
```bash
sed -n '2p' dosya.txt
```

### 4. Birden Fazla Değişiklik Yapma
Birden fazla kelimeyi değiştirmek için:
```bash
sed -e 's/eski/yeni/' -e 's/başka/yeni2/' dosya.txt
```

## İpuçları
- `sed` ile çalışırken, dosyalarınızın yedeğini almak iyi bir uygulamadır, özellikle `-i` seçeneğini kullanıyorsanız.
- Komutları test etmek için önce `-n` seçeneği ile çıktıyı kontrol edin.
- Karmaşık düzenlemeler için düzenli ifadeleri kullanmayı öğrenmek, `sed`'in gücünü artırır.