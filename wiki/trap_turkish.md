# [Türkçe] Debian Almquist Shell (dash) trap Kullanımı: Sinyal yakalama ve işleme

## Genel Bakış
`trap` komutu, bir shell script'inde belirli sinyalleri yakalamak ve bu sinyallere yanıt vermek için kullanılır. Bu, script'inizin belirli durumlarla başa çıkmasını sağlar, örneğin bir kullanıcı script'i durdurmaya çalıştığında veya bir hata oluştuğunda.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
trap [options] [arguments]
```

## Yaygın Seçenekler
- `SIGINT`: Kullanıcı tarafından Ctrl+C ile gönderilen kesme sinyali.
- `SIGTERM`: İşlemi sonlandırmak için gönderilen sinyal.
- `EXIT`: Script sona erdiğinde çalıştırılacak komutlar.
- `ERR`: Bir hata oluştuğunda çalıştırılacak komutlar.

## Yaygın Örnekler

1. **Ctrl+C ile script'i durdurma:**
   Aşağıdaki örnekte, Ctrl+C ile script durdurulduğunda bir mesaj yazdırılır.
   ```bash
   trap 'echo "Script durduruldu."' SIGINT
   while true; do
       echo "Çalışıyor..."
       sleep 1
   done
   ```

2. **Script sona erdiğinde temizlik yapma:**
   Script sona erdiğinde geçici dosyaları silmek için kullanılabilir.
   ```bash
   trap 'rm -f /tmp/tempfile; echo "Geçici dosya silindi."' EXIT
   touch /tmp/tempfile
   echo "Script çalışıyor..."
   sleep 5
   ```

3. **Hata durumunda mesaj gösterme:**
   Bir hata oluştuğunda kullanıcıya bilgi vermek için kullanılabilir.
   ```bash
   trap 'echo "Bir hata oluştu!"' ERR
   false  # Bu komut hata döndürür
   ```

## İpuçları
- `trap` komutunu kullanırken, hangi sinyalleri yakalamak istediğinizi dikkatlice belirleyin.
- Hata durumlarında kullanıcıya bilgi vermek, script'inizle etkileşimde bulunmayı kolaylaştırır.
- Script'inizin sonunda `EXIT` sinyalini kullanarak temizlik işlemleri yapmayı unutmayın.