# [Türkçe] Debian Almquist Shell (dash) pkill Kullanımı: Süreçleri adlarına göre sonlandırma

## Genel Bakış
`pkill` komutu, belirtilen isim veya özelliklere göre çalışan süreçleri sonlandırmak için kullanılır. Bu, belirli bir uygulamayı veya işlemi kolayca kapatmanıza olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
pkill [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f`: Tam komut satırını kullanarak eşleşme yapar.
- `-n`: En son başlatılan süreci sonlandırır.
- `-o`: En eski başlatılan süreci sonlandırır.
- `-u`: Belirtilen kullanıcıya ait süreçleri sonlandırır.

## Yaygın Örnekler
Aşağıda `pkill` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir süreç adını kullanarak süreci sonlandırma:
   ```bash
   pkill firefox
   ```

2. Tam komut satırına göre süreci sonlandırma:
   ```bash
   pkill -f "python my_script.py"
   ```

3, Belirli bir kullanıcıya ait süreçleri sonlandırma:
   ```bash
   pkill -u kullanıcı_adı
   ```

4. En son başlatılan süreci sonlandırma:
   ```bash
   pkill -n bash
   ```

5. En eski başlatılan süreci sonlandırma:
   ```bash
   pkill -o ssh
   ```

## İpuçları
- `pkill` kullanmadan önce, hangi süreçlerin çalıştığını görmek için `ps` komutunu kullanabilirsiniz.
- Süreçleri sonlandırmadan önce dikkatli olun; yanlış bir süreç sonlandırmak sisteminize zarar verebilir.
- `pkill` komutunu `-n` veya `-o` seçenekleriyle kullanarak belirli süreçleri hedef alabilirsiniz, bu da daha kontrollü bir kapatma sağlar.