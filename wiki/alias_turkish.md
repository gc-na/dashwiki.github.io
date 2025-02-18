# [Türkçe] Debian Almquist Shell (dash) alias kullanımı: Komut kısayolları oluşturma

## Genel Bakış
`alias` komutu, kullanıcıların sık kullandıkları komutlar için kısayollar oluşturmasına olanak tanır. Bu sayede uzun ve karmaşık komutları daha kısa ve kolay hatırlanabilir hale getirebilirsiniz.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
alias [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Mevcut tüm alias'ları listelemek için kullanılır.
- `--help`: Komut hakkında yardım bilgisi gösterir.

## Yaygın Örnekler
Aşağıda `alias` komutunun bazı pratik örnekleri verilmiştir:

1. **Basit bir alias oluşturma:**
   ```bash
   alias ll='ls -la'
   ```
   Bu komut, `ll` yazdığınızda `ls -la` komutunu çalıştırır.

2. **Bir alias silme:**
   ```bash
   unalias ll
   ```
   Bu komut, `ll` alias'ını kaldırır.

3. **Alias'ları listeleme:**
   ```bash
   alias -p
   ```
   Bu komut, tanımlı olan tüm alias'ları gösterir.

4. **Alias'ı geçici olarak kullanma:**
   ```bash
   alias gs='git status'
   ```
   Bu komut, `gs` yazdığınızda `git status` komutunu çalıştırır.

## İpuçları
- Alias'larınızı kalıcı hale getirmek için, bunları `~/.bashrc` veya `~/.profile` dosyanıza ekleyin.
- Kısa ve anlamlı isimler kullanarak alias'larınızı daha kolay hatırlanabilir hale getirin.
- Sık kullandığınız komutları alias ile tanımlayarak zaman kazanabilirsiniz.