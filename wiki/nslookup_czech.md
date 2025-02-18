# [Debian] Debian Almquist Shell (dash) nslookup použití: Získání informací o DNS

## Přehled
Příkaz `nslookup` slouží k dotazování na informace o doménových jménech a jejich odpovídajících IP adresách pomocí systému DNS (Domain Name System). Umožňuje uživatelům ověřit, zda jsou domény správně nakonfigurovány a jaké IP adresy jsou s nimi spojeny.

## Použití
Základní syntaxe příkazu `nslookup` je následující:

```bash
nslookup [možnosti] [argumenty]
```

## Běžné možnosti
- `-type=typ`: Určuje typ DNS záznamu, který chcete vyhledat (např. A, AAAA, MX).
- `-timeout=sekundy`: Nastavuje časový limit pro čekání na odpověď.
- `-retry=počet`: Určuje počet pokusů o dotazování, pokud nedojde k úspěšné odpovědi.

## Běžné příklady
1. Základní dotaz na IP adresu domény:
   ```bash
   nslookup example.com
   ```

2. Dotaz na konkrétní typ záznamu (např. MX):
   ```bash
   nslookup -type=MX example.com
   ```

3. Dotaz na doménu s nastaveným časovým limitem:
   ```bash
   nslookup -timeout=5 example.com
   ```

4. Dotaz na IP adresu pomocí specifického DNS serveru:
   ```bash
   nslookup example.com 8.8.8.8
   ```

## Tipy
- Používejte `nslookup` pro rychlé ověření DNS záznamů, pokud máte podezření na problémy s připojením.
- Zkuste různé typy záznamů, abyste získali komplexnější pohled na doménu.
- Pokud se často dotazujete na stejnou doménu, můžete si uložit výsledky do souboru pro pozdější analýzu.