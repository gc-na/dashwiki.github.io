# [Český] Debian Almquist Shell (dash) gunzip použití: Decompressing gzip files

## Přehled
Příkaz `gunzip` slouží k dekompresi souborů, které byly komprimovány pomocí algoritmu gzip. Tento příkaz odstraní kompresi a obnoví původní soubor.

## Použití
Základní syntaxe příkazu je následující:

```
gunzip [možnosti] [argumenty]
```

## Běžné možnosti
- `-c`: Výstup dekomprimovaného obsahu na standardní výstup (stdout) místo přepsání souboru.
- `-f`: Přepsání existujících souborů bez dotazu.
- `-k`: Zachování původního souboru po dekompresi.
- `-r`: Rekurzivní dekomprese souborů v adresáři.

## Běžné příklady
- Dekomprese souboru `soubor.gz`:

  ```bash
  gunzip soubor.gz
  ```

- Dekomprese souboru a zachování původního souboru:

  ```bash
  gunzip -k soubor.gz
  ```

- Dekomprese všech gzip souborů v aktuálním adresáři:

  ```bash
  gunzip *.gz
  ```

- Dekomprese souboru a výstup na standardní výstup:

  ```bash
  gunzip -c soubor.gz
  ```

## Tipy
- Před použitím `gunzip` se ujistěte, že máte zálohu důležitých souborů, zejména pokud používáte možnost `-f`.
- Pokud potřebujete dekomprimovat více souborů, můžete použít zástupné znaky, jako je `*.gz`, pro efektivnější práci.
- Pro zajištění, že nedojde k nechtěnému přepsání souborů, je dobré používat možnost `-k`.