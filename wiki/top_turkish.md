# [Türkçe] Debian Almquist Shell (dash) top Kullanımı: Sistem kaynaklarını izleme aracı

## Genel Bakış
`top` komutu, sistemdeki işlemleri ve kaynak kullanımını gerçek zamanlı olarak izlemek için kullanılan bir araçtır. Bu komut, CPU, bellek ve diğer sistem kaynaklarının kullanımını gösterir, böylece kullanıcılar sistem performansını değerlendirebilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
top [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-d [saniye]`: Güncelleme aralığını saniye cinsinden ayarlamak için kullanılır.
- `-n [sayı]`: Belirtilen sayı kadar güncelleme yaptıktan sonra çıkmak için kullanılır.
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait işlemleri görüntülemek için kullanılır.
- `-p [PID]`: Belirtilen işlem kimliğine (PID) sahip işlemi izlemek için kullanılır.

## Yaygın Örnekler
Aşağıda `top` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Temel top komutunu çalıştırma:**
   ```bash
   top
   ```

2. **Güncelleme aralığını 2 saniye olarak ayarlama:**
   ```bash
   top -d 2
   ```

3. **Sadece belirli bir kullanıcıya ait işlemleri görüntüleme:**
   ```bash
   top -u kullanıcı_adı
   ```

4. **Belirli bir işlem kimliğini izleme:**
   ```bash
   top -p 1234
   ```

5. **5 güncellemeden sonra çıkma:**
   ```bash
   top -n 5
   ```

## İpuçları
- `top` arayüzünde, `h` tuşuna basarak yardım alabilirsiniz.
- `k` tuşuna basarak bir işlemi sonlandırmak için PID'yi girin.
- `M` tuşuna basarak işlemleri bellek kullanımına göre sıralayabilirsiniz.
- `P` tuşuna basarak işlemleri CPU kullanımına göre sıralayabilirsiniz.

Bu bilgilerle `top` komutunu etkili bir şekilde kullanarak sistem kaynaklarınızı izleyebilir ve yönetebilirsiniz.