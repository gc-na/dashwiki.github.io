# [Český] Debian Almquist Shell (dash) find použití: Hledání názvů souborů

## Přehled
Příkaz `find` slouží k vyhledávání souborů a adresářů v hierarchii souborového systému na základě různých kritérií, jako jsou jméno, typ, velikost nebo datum poslední změny.

## Použití
Základní syntaxe příkazu `find` je následující:

```bash
find [možnosti] [argumenty]
```

## Běžné možnosti
- `-name <název>`: Hledá soubory podle názvu.
- `-type <typ>`: Určuje typ souboru (např. `f` pro soubory, `d` pro adresáře).
- `-size <velikost>`: Hledá soubory podle velikosti.
- `-mtime <dny>`: Hledá soubory podle data poslední změny (např. `-mtime -7` pro soubory změněné v posledních 7 dnech).
- `-exec <příkaz> {} \;`: Provádí příkaz na každém nalezeném souboru.

## Běžné příklady
- Hledání souboru s konkrétním názvem:
  ```bash
  find /cesta/k/adresáři -name "soubor.txt"
  ```

- Hledání všech adresářů:
  ```bash
  find /cesta/k/adresáři -type d
  ```

- Hledání souborů větších než 1 MB:
  ```bash
  find /cesta/k/adresáři -size +1M
  ```

- Hledání souborů změněných za poslední 3 dny:
  ```bash
  find /cesta/k/adresáři -mtime -3
  ```

- Hledání a odstranění prázdných adresářů:
  ```bash
  find /cesta/k/adresáři -type d -empty -exec rmdir {} \;
  ```

## Tipy
- Používejte `-iname` místo `-name`, pokud chcete ignorovat velikost písmen při hledání názvů souborů.
- Kombinujte možnosti pro efektivnější vyhledávání, například `find /cesta -type f -size +500k -mtime -7` pro hledání souborů větších než 500 kB, které byly změněny v posledních 7 dnech.
- Vždy testujte příkazy s `-print` před použitím `-exec`, abyste viděli, které soubory budou ovlivněny.