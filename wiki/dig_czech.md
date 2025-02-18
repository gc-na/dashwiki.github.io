# [Český] Debian Almquist Shell (dash) dig <Použití: Získání informací o DNS>

## Přehled
Příkaz `dig` (Domain Information Groper) slouží k dotazování na DNS (Domain Name System) a poskytuje podrobné informace o doménách, IP adresách a dalších souvisejících záznamech. Je užitečný pro správu sítí a diagnostiku problémů s DNS.

## Použití
Základní syntaxe příkazu `dig` je následující:

```
dig [možnosti] [argumenty]
```

## Běžné možnosti
- `@server` - Určuje DNS server, na který se dotazujete.
- `-t typ` - Určuje typ DNS záznamu (např. A, AAAA, MX, TXT).
- `+short` - Zobrazí zjednodušený výstup.
- `+trace` - Sleduje cestu dotazu přes DNS servery.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `dig`:

1. Získání A záznamu pro doménu:
   ```bash
   dig example.com A
   ```

2. Získání MX záznamu pro doménu:
   ```bash
   dig example.com MX
   ```

3. Dotaz na konkrétní DNS server:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. Zjednodušený výstup pro A záznam:
   ```bash
   dig +short example.com
   ```

5. Sledování cesty dotazu:
   ```bash
   dig +trace example.com
   ```

## Tipy
- Používejte `+short`, pokud potřebujete rychlý a přehledný výstup.
- Zkuste různé typy záznamů (A, AAAA, MX, TXT) pro získání různých informací o doméně.
- Pokud máte problémy s DNS, použijte možnost `+trace` pro diagnostiku cesty dotazu.