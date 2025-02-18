# [Český] Debian Almquist Shell (dash) gzip Použití: Komprimace souborů

## Přehled
Příkaz `gzip` slouží k komprimaci souborů pomocí algoritmu DEFLATE. Je široce používán pro zmenšení velikosti souborů, což usnadňuje jejich ukládání a přenos.

## Použití
Základní syntaxe příkazu je následující:

```bash
gzip [možnosti] [argumenty]
```

## Běžné možnosti
- `-d` nebo `--decompress`: Rozbalí komprimovaný soubor.
- `-k` nebo `--keep`: Zachová původní soubor po komprimaci.
- `-v` nebo `--verbose`: Zobrazí podrobnosti o kompresi.
- `-f` nebo `--force`: Přepíše existující soubory bez dotazu.

## Běžné příklady
1. Komprimace souboru:
   ```bash
   gzip soubor.txt
   ```

2. Rozbalení komprimovaného souboru:
   ```bash
   gzip -d soubor.txt.gz
   ```

3. Komprimace souboru a zachování původního souboru:
   ```bash
   gzip -k soubor.txt
   ```

4. Zobrazení podrobností o kompresi:
   ```bash
   gzip -v soubor.txt
   ```

5. Přepsání existujícího souboru bez dotazu:
   ```bash
   gzip -f soubor.txt
   ```

## Tipy
- Při komprimaci velkých souborů se ujistěte, že máte dostatek volného místa na disku.
- Používejte volbu `-k`, pokud chcete mít k dispozici jak původní, tak komprimovaný soubor.
- Pro efektivnější práci s více soubory můžete použít zástupné znaky, například `gzip *.txt` pro komprimaci všech textových souborů v adresáři.