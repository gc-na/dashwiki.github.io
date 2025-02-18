# [Türkçe] Debian Almquist Shell (dash) export Kullanımı: Ortam değişkenlerini ayarlama

## Overview
`export` komutu, bir ortam değişkenini tanımlamak ve bu değişkeni alt süreçlere (child processes) aktarmak için kullanılır. Bu, shell oturumu boyunca değişkenlerin kullanılmasını sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```sh
export [options] [arguments]
```

## Common Options
- `-n`: Belirtilen değişkenin export edilmesini iptal eder.
- `-p`: Tüm export edilmiş değişkenleri listelemek için kullanılır.

## Common Examples
Aşağıda `export` komutunun yaygın kullanım örnekleri bulunmaktadır:

1. Basit bir ortam değişkeni tanımlama ve export etme:
   ```sh
   export MY_VAR="Merhaba Dünya"
   ```

2. Daha önce tanımlanmış bir değişkeni export etme:
   ```sh
   MY_VAR="Merhaba Dünya"
   export MY_VAR
   ```

3. Birden fazla değişkeni aynı anda export etme:
   ```sh
   export VAR1="Değer1" VAR2="Değer2"
   ```

4. Export edilmiş değişkenleri listeleme:
   ```sh
   export -p
   ```

5. Bir değişkenin export edilmesini iptal etme:
   ```sh
   export -n MY_VAR
   ```

## Tips
- Ortam değişkenlerini export etmeden önce, değişkenin doğru bir şekilde tanımlandığından emin olun.
- Değişken adlarının büyük harfle başlaması, genellikle daha iyi bir uygulama olarak kabul edilir.
- `export` komutunu kullanarak, shell oturumunuzda yaptığınız değişikliklerin alt süreçlerde de geçerli olmasını sağlayabilirsiniz.