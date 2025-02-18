# [Český] Debian Almquist Shell (dash) bzip2 použití: Komprimace souborů

## Přehled
Příkaz `bzip2` slouží k efektivní kompresi souborů pomocí algoritmu bzip2. Tento nástroj je oblíbený pro svou schopnost dosahovat vysokého stupně komprese, což šetří místo na disku.

## Použití
Základní syntaxe příkazu je následující:

```bash
bzip2 [možnosti] [argumenty]
```

## Běžné možnosti
- `-d`, `--decompress`: Rozbalí komprimovaný soubor.
- `-k`, `--keep`: Udržuje původní soubor po kompresi.
- `-f`, `--force`: Přepíše existující soubory bez dotazu.
- `-v`, `--verbose`: Zobrazí podrobnosti o procesu komprese.

## Běžné příklady
1. Komprese souboru:
   ```bash
   bzip2 soubor.txt
   ```
   Tento příkaz vytvoří komprimovaný soubor `soubor.txt.bz2`.

2. Rozbalení komprimovaného souboru:
   ```bash
   bzip2 -d soubor.txt.bz2
   ```
   Tento příkaz obnoví původní soubor `soubor.txt`.

3. Komprese souboru a zachování původního:
   ```bash
   bzip2 -k soubor.txt
   ```
   Původní soubor zůstane a bude vytvořen komprimovaný soubor `soubor.txt.bz2`.

4. Komprese více souborů najednou:
   ```bash
   bzip2 soubor1.txt soubor2.txt
   ```
   Tento příkaz zkomprimuje oba soubory.

5. Zobrazení podrobností o kompresi:
   ```bash
   bzip2 -v soubor.txt
   ```
   Tento příkaz ukáže informace o procesu komprese.

## Tipy
- Používejte možnost `-k`, pokud chcete zachovat původní soubory po kompresi.
- Při rozbalování souborů se ujistěte, že máte dostatek místa na disku pro obnovené soubory.
- Pro zrychlení komprese můžete experimentovat s různými úrovněmi komprese pomocí `-1` (nejrychlejší) až `-9` (nejlepší komprese).