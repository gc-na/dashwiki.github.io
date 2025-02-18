# [Türkçe] Debian Almquist Shell (dash) strace Kullanımı: Sistem çağrılarını izleme aracı

## Genel Bakış
`strace`, bir programın sistem çağrılarını ve sinyallerini izlemek için kullanılan bir komuttur. Bu komut, bir programın çalışma sırasında hangi sistem kaynaklarını kullandığını anlamak ve hata ayıklamak için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
strace [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c`: Her sistem çağrısının istatistiklerini toplar ve özetler.
- `-e`: Belirli bir sistem çağrısını izlemek için kullanılır. Örneğin, `-e trace=open` sadece `open` çağrılarını izler.
- `-o <dosya>`: Çıktıyı belirtilen dosyaya yönlendirir.
- `-p <PID>`: Belirli bir işlem kimliğini (PID) izler.
- `-f`: Alt süreçleri de izler.

## Yaygın Örnekler
Aşağıda `strace` komutunun bazı pratik kullanımları verilmiştir:

1. Bir programın sistem çağrılarını izlemek:
   ```bash
   strace ls
   ```

2. Çıktıyı bir dosyaya yönlendirmek:
   ```bash
   strace -o strace_output.txt ls
   ```

3. Belirli bir sistem çağrısını izlemek:
   ```bash
   strace -e trace=open ls
   ```

4. Çalışan bir süreci izlemek:
   ```bash
   strace -p 1234
   ```

5. İstatistikleri toplamak:
   ```bash
   strace -c ls
   ```

## İpuçları
- `strace` çıktısını daha iyi anlamak için `grep` ile filtreleme yapabilirsiniz. Örneğin, sadece `open` çağrılarını görmek için:
  ```bash
  strace ls | grep open
  ```
- Uzun süreli izlemelerde çıktıyı dosyaya yönlendirmek, terminaldeki karmaşayı azaltır.
- `strace` kullanırken, izlenen programın performansını etkileyebileceğini unutmayın. Bu nedenle, üretim ortamlarında dikkatli kullanılmalıdır.