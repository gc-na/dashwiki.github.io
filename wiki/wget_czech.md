# [Český] Debian Almquist Shell (dash) wget použití: Stahování souborů z webu

## Přehled
Příkaz `wget` je nástroj pro stahování souborů z webu pomocí protokolů HTTP, HTTPS a FTP. Umožňuje uživatelům snadno stahovat jednotlivé soubory nebo dokonce celé webové stránky.

## Použití
Základní syntaxe příkazu `wget` je následující:

```
wget [možnosti] [argumenty]
```

## Běžné možnosti
- `-O [soubor]`: Umožňuje uložit stažený soubor pod zadaným názvem.
- `-c`: Pokračuje ve stahování přerušeného souboru.
- `-r`: Stahuje soubory rekurzivně (včetně odkazů na další stránky).
- `-q`: Spouští wget v tichém režimu, bez výstupu na obrazovku.
- `--limit-rate=[rychlost]`: Omezí rychlost stahování na zadanou hodnotu.

## Běžné příklady
Stahování jednotlivého souboru:
```bash
wget https://example.com/soubor.txt
```

Uložení souboru pod jiným názvem:
```bash
wget -O novy_nazev.txt https://example.com/soubor.txt
```

Pokračování ve stahování přerušeného souboru:
```bash
wget -c https://example.com/soubor.txt
```

Rekurzivní stahování celého webu:
```bash
wget -r https://example.com/
```

Stahování s omezením rychlosti:
```bash
wget --limit-rate=200k https://example.com/soubor.txt
```

## Tipy
- Při stahování velkých souborů zvažte použití možnosti `-c`, abyste mohli pokračovat ve stahování, pokud dojde k přerušení.
- Používejte `-q` pro tichý režim, pokud nechcete, aby se na obrazovce zobrazovaly výstupy.
- Při rekurzivním stahování buďte opatrní, abyste nezatížili server příliš mnoha požadavky.