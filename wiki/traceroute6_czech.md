# [Český] Debian Almquist Shell (dash) traceroute6 použití: Zjistit cestu IPv6 paketů

## Přehled
Příkaz `traceroute6` slouží k diagnostice sítě a zobrazuje cestu, kterou IPv6 pakety procházejí z vašeho počítače na cílovou adresu. Pomocí tohoto příkazu můžete zjistit, jaké servery a směrovače se nacházejí mezi vámi a cílovým uzlem.

## Použití
Základní syntaxe příkazu je následující:

```bash
traceroute6 [možnosti] [argumenty]
```

## Běžné možnosti
- `-m <max_hops>`: Nastaví maximální počet skoků, které traceroute provede.
- `-w <timeout>`: Nastaví časový limit pro čekání na odpověď.
- `-q <nqueries>`: Určuje počet dotazů, které se mají odeslat na každý skok.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `traceroute6`:

1. Základní použití pro sledování cesty k cílové adrese:
   ```bash
   traceroute6 google.com
   ```

2. S nastavením maximálního počtu skoků na 15:
   ```bash
   traceroute6 -m 15 google.com
   ```

3. S nastavením časového limitu na 2 sekundy:
   ```bash
   traceroute6 -w 2 google.com
   ```

4. Odeslání 3 dotazů na každý skok:
   ```bash
   traceroute6 -q 3 google.com
   ```

## Tipy
- Při sledování cesty k cílové adrese zkuste použít různé možnosti, abyste získali podrobnější informace.
- Pokud máte problémy s dosažením určitého uzlu, zkuste zvýšit časový limit pro odpovědi.
- Ujistěte se, že máte povolený IPv6 protokol na vašem zařízení, jinak příkaz nebude fungovat správně.