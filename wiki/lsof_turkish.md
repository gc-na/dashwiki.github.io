# [Türkçe] Debian Almquist Shell (dash) lsof Kullanımı: Açık dosyaları listeleme

## Genel Bakış
`lsof` (List Open Files) komutu, sistemde açık olan dosyaları ve bu dosyaları kullanan süreçleri listelemek için kullanılır. Bu komut, dosya tanımlayıcıları, süreç kimlikleri ve dosya yolları gibi bilgileri sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
lsof [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait açık dosyaları gösterir.
- `-p [PID]`: Belirtilen süreç kimliğine (PID) ait açık dosyaları gösterir.
- `-i`: Ağ bağlantılarına ait açık dosyaları gösterir.
- `-t`: Sadece süreç kimliklerini (PID) gösterir, daha az bilgi verir.
- `+D [dizin]`: Belirtilen dizinde bulunan tüm dosyaları ve alt dizinlerdeki dosyaları listeler.

## Yaygın Örnekler
Aşağıda `lsof` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Tüm Açık Dosyaları Listeleme
```bash
lsof
```

### 2. Belirli Bir Kullanıcıya Ait Açık Dosyaları Listeleme
```bash
lsof -u kullanıcı_adı
```

### 3. Belirli Bir Süreç Kimliğine Ait Açık Dosyaları Listeleme
```bash
lsof -p 1234
```

### 4. Ağ Bağlantılarına Ait Açık Dosyaları Listeleme
```bash
lsof -i
```

### 5. Belirli Bir Dizinde Açık Dosyaları Listeleme
```bash
lsof +D /path/to/directory
```

## İpuçları
- `lsof` komutunu kullanmadan önce, yeterli izinlere sahip olduğunuzdan emin olun; bazı dosyalar ve süreçler için erişim kısıtlamaları olabilir.
- `lsof` çıktısını daha okunabilir hale getirmek için `grep` ile filtreleme yapabilirsiniz. Örneğin, belirli bir dosya adını aramak için:
  ```bash
  lsof | grep dosya_adı
  ```
- Ağ bağlantılarını izlemek için `lsof -i` komutunu düzenli olarak kullanarak sisteminizdeki aktif bağlantıları takip edebilirsiniz.