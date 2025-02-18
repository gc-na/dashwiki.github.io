# [Türkçe] Debian Almquist Shell (dash) awk Kullanımı: Metin işleme aracı

## Genel Bakış
`awk`, metin dosyalarını işlemek ve analiz etmek için kullanılan güçlü bir komut satırı aracıdır. Genellikle verileri düzenlemek, filtrelemek ve biçimlendirmek için kullanılır. `awk`, belirli bir desenle eşleşen satırları bulup, bu satırlardaki verileri işleyebilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
awk [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-F`: Alan ayırıcıyı belirtir. Varsayılan olarak boşluk veya sekme kullanılır.
- `-v`: Değişken tanımlamak için kullanılır.
- `-f`: Bir dosyadan `awk` programı yüklemek için kullanılır.
- `-W`: `awk`'ın davranışını değiştiren seçenekler sunar.

## Yaygın Örnekler
1. **Bir dosyadaki tüm satırları yazdırma:**
   ```bash
   awk '{print}' dosya.txt
   ```

2. **Belirli bir alanı yazdırma (örneğin, ikinci alan):**
   ```bash
   awk '{print $2}' dosya.txt
   ```

3. **Bir koşula göre filtreleme (örneğin, 100'den büyük sayıları yazdırma):**
   ```bash
   awk '$1 > 100 {print}' dosya.txt
   ```

4. **Alan ayırıcıyı değiştirme (örneğin, virgül ile ayrılmış dosya):**
   ```bash
   awk -F',' '{print $1}' dosya.csv
   ```

5. **Bir değişken kullanma:**
   ```bash
   awk -v limit=100 '$1 > limit {print}' dosya.txt
   ```

## İpuçları
- `awk` komutunu daha okunabilir hale getirmek için, karmaşık işlemleri bir dosyaya yazmayı düşünün.
- Alanları doğru bir şekilde ayırmak için `-F` seçeneğini kullanarak özel ayırıcılar belirleyin.
- `awk`'ın çıktısını başka komutlarla birleştirerek daha karmaşık veri işleme görevleri gerçekleştirebilirsiniz.