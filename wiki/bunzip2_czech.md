# [Český] Debian Almquist Shell (dash) bunzip2 použití: Decompressing bzip2 files

## Přehled
Příkaz `bunzip2` slouží k dekompresi souborů, které byly komprimovány pomocí algoritmu bzip2. Tento nástroj je užitečný pro uvolnění místa na disku a pro práci se soubory, které jsou uloženy ve zkomprimované podobě.

## Použití
Základní syntaxe příkazu `bunzip2` je následující:

```bash
bunzip2 [možnosti] [argumenty]
```

## Běžné možnosti
- `-k`, `--keep`: Zachová původní soubor po dekompresi.
- `-f`, `--force`: Přepíše existující soubory bez dotazu.
- `-v`, `--verbose`: Zobrazí podrobnosti o procesu dekomprese.

## Běžné příklady
1. **Dekomprese souboru**:
   Chcete-li dekomprimovat soubor `soubor.bz2`, použijte následující příkaz:
   ```bash
   bunzip2 soubor.bz2
   ```

2. **Zachování původního souboru**:
   Pokud chcete dekomprimovat soubor a zároveň zachovat původní soubor, použijte možnost `-k`:
   ```bash
   bunzip2 -k soubor.bz2
   ```

3. **Dekomprese více souborů**:
   Můžete také dekomprimovat více souborů najednou:
   ```bash
   bunzip2 soubor1.bz2 soubor2.bz2
   ```

4. **Přepsání existujícího souboru**:
   Pokud chcete dekomprimovat a přepsat existující soubor, použijte možnost `-f`:
   ```bash
   bunzip2 -f soubor.bz2
   ```

## Tipy
- Před dekompresí se ujistěte, že máte dostatek volného místa na disku, protože dekomprimovaný soubor může být výrazně větší než zkomprimovaný.
- Pokud často pracujete se zkomprimovanými soubory, zvažte použití skriptu, který automatizuje proces dekomprese a zálohování původních souborů.
- Vždy si ověřte, že dekomprimovaný soubor je v pořádku, zejména pokud byl stažen z internetu.