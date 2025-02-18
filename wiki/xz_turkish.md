# [Türkçe] Debian Almquist Shell (dash) xz Kullanımı: Dosyaları sıkıştırma ve açma

## Genel Bakış
`xz` komutu, dosyaları sıkıştırmak ve açmak için kullanılan bir araçtır. Yüksek sıkıştırma oranları sunarak disk alanından tasarruf etmenizi sağlar. Genellikle büyük dosyaların boyutunu azaltmak için tercih edilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
xz [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-d`, `--decompress`: Sıkıştırılmış dosyayı açar.
- `-k`, `--keep`: Orijinal dosyayı koruyarak sıkıştırma işlemi yapar.
- `-f`, `--force`: Var olan dosyaların üzerine yazmak için zorlar.
- `-z`, `--compress`: Dosyayı sıkıştırır (varsayılan davranış).
- `-t`, `--test`: Sıkıştırılmış dosyanın bütünlüğünü kontrol eder.

## Yaygın Örnekler
Aşağıda `xz` komutunun bazı pratik kullanımları verilmiştir:

### 1. Dosya Sıkıştırma
Bir dosyayı sıkıştırmak için:
```bash
xz dosya.txt
```

### 2. Dosya Açma
Sıkıştırılmış bir dosyayı açmak için:
```bash
xz -d dosya.txt.xz
```

### 3. Orijinal Dosyayı Koruyarak Sıkıştırma
Orijinal dosyayı koruyarak sıkıştırmak için:
```bash
xz -k dosya.txt
```

### 4. Sıkıştırılmış Dosyanın Bütünlüğünü Kontrol Etme
Bir sıkıştırılmış dosyanın bütünlüğünü kontrol etmek için:
```bash
xz -t dosya.txt.xz
```

## İpuçları
- Sıkıştırma işlemi sırasında `-k` seçeneğini kullanarak orijinal dosyayı kaybetmemek için dikkat edin.
- Büyük dosyalarla çalışırken, sıkıştırma işleminin zaman alabileceğini unutmayın; bu nedenle, işlemi arka planda çalıştırmak isteyebilirsiniz.
- Sıkıştırma oranını artırmak için `-9` seçeneğini kullanabilirsiniz, ancak bu işlem daha fazla zaman alabilir:
```bash
xz -9 dosya.txt
```