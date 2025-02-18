# [Český] Debian Almquist Shell (dash) ping použití: Ověření dostupnosti sítě

## Přehled
Příkaz `ping` slouží k testování dostupnosti síťových zařízení. Odesílá ICMP echo požadavky na cílovou adresu a měří dobu potřebnou k obdržení odpovědi, což umožňuje uživatelům zjistit, zda je zařízení dostupné a jaká je kvalita spojení.

## Použití
Základní syntaxe příkazu `ping` je následující:

```bash
ping [možnosti] [argumenty]
```

## Běžné možnosti
- `-c [počet]`: Odeslat pouze zadaný počet echo požadavků.
- `-i [interval]`: Nastavit interval mezi odesíláním požadavků v sekundách.
- `-s [velikost]`: Nastavit velikost odesílaného paketu.
- `-t [TTL]`: Nastavit hodnotu TTL (Time To Live) pro pakety.

## Běžné příklady
1. Odeslání nekonečného počtu echo požadavků na adresu `example.com`:
   ```bash
   ping example.com
   ```

2. Odeslání 5 echo požadavků:
   ```bash
   ping -c 5 example.com
   ```

3. Odeslání echo požadavků s intervalem 2 sekundy:
   ```bash
   ping -i 2 example.com
   ```

4. Odeslání echo požadavků s velikostí paketu 100 bytů:
   ```bash
   ping -s 100 example.com
   ```

## Tipy
- Používejte `-c` pro omezení počtu požadavků, abyste nezaplnili síť zbytečnými daty.
- Pokud testujete latenci mezi dvěma zařízeními, zkuste použít různé velikosti paketů pomocí `-s`, abyste zjistili, jak se chování sítě mění.
- Příkaz `ping` může být užitečný při diagnostice problémů se sítí, takže ho používejte jako první krok při odstraňování potíží.