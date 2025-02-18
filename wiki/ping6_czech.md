# [Debian] Debian Almquist Shell (dash) ping6 použití: Ověření dostupnosti IPv6 adres

## Přehled
Příkaz `ping6` slouží k testování dostupnosti IPv6 adres. Odesílá ICMPv6 echo požadavky na cílovou adresu a měří dobu odezvy. Tento nástroj je užitečný pro diagnostiku síťových problémů a ověřování, zda je cílová adresa dostupná.

## Použití
Základní syntaxe příkazu je následující:

```
ping6 [možnosti] [argumenty]
```

## Běžné možnosti
- `-c [číslo]`: Určuje počet echo požadavků, které se mají odeslat.
- `-i [čas]`: Nastavuje interval mezi odesíláním požadavků v sekundách.
- `-w [čas]`: Určuje maximální dobu trvání testu v sekundách.
- `-s [velikost]`: Nastavuje velikost datového paketu v bajtech.

## Běžné příklady
1. Odeslání 4 echo požadavků na IPv6 adresu:
   ```bash
   ping6 -c 4 2001:db8::1
   ```

2. Odesílání požadavků s intervalem 2 sekundy:
   ```bash
   ping6 -i 2 2001:db8::1
   ```

3. Odeslání požadavků a nastavení maximální doby trvání na 10 sekund:
   ```bash
   ping6 -w 10 2001:db8::1
   ```

4. Odeslání echo požadavků s vlastní velikostí paketu:
   ```bash
   ping6 -s 1280 2001:db8::1
   ```

## Tipy
- Používejte možnost `-c`, pokud chcete omezit počet požadavků a zabránit nekonečnému běhu příkazu.
- Zkontrolujte, zda máte správně nakonfigurovanou IPv6 adresaci na vašem zařízení, než začnete testovat.
- Pokud se pokoušíte diagnostikovat problémy s připojením, zkuste pingovat různé IPv6 adresy, abyste zjistili, zda je problém specifický pro určitou adresu nebo obecnější.