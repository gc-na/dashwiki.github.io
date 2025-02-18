# [Český] Debian Almquist Shell (dash) tar <Použití>: Komprimace a archivace souborů

## Přehled
Příkaz `tar` slouží k vytváření archivů a jejich extrakci. Umožňuje shromáždit více souborů do jednoho souboru, což usnadňuje jejich přenos a zálohování.

## Použití
Základní syntaxe příkazu `tar` je následující:

```bash
tar [možnosti] [argumenty]
```

## Běžné možnosti
- `-c`: Vytvoření nového archivu.
- `-x`: Extrakce souborů z archivu.
- `-f`: Určení názvu archivu.
- `-v`: Zobrazí podrobnosti o procesu (verbose).
- `-z`: Komprese pomocí gzip.
- `-j`: Komprese pomocí bzip2.

## Běžné příklady
1. Vytvoření archivu:
   ```bash
   tar -cvf archiv.tar /cesta/k/souborům
   ```

2. Extrakce archivu:
   ```bash
   tar -xvf archiv.tar
   ```

3. Vytvoření komprimovaného archivu pomocí gzip:
   ```bash
   tar -czvf archiv.tar.gz /cesta/k/souborům
   ```

4. Extrakce komprimovaného archivu:
   ```bash
   tar -xzvf archiv.tar.gz
   ```

5. Vytvoření archivu s bzip2 kompresí:
   ```bash
   tar -cjvf archiv.tar.bz2 /cesta/k/souborům
   ```

## Tipy
- Při vytváření archivu je dobré používat příponu `.tar`, `.tar.gz` nebo `.tar.bz2` pro snadnější identifikaci.
- Před extrakcí archivu zkontrolujte jeho obsah pomocí `tar -tvf archiv.tar`, abyste se ujistili, co obsahuje.
- Pokud archivujete velké množství souborů, zvažte použití komprese, abyste ušetřili místo na disku.