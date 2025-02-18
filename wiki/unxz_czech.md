# [Český] Debian Almquist Shell (dash) unxz použití: Rozbalení souborů ve formátu .xz

## Přehled
Příkaz `unxz` slouží k rozbalení souborů komprimovaných pomocí algoritmu XZ. Tento příkaz odstraní příponu `.xz` a obnoví původní soubor.

## Použití
Základní syntaxe příkazu je následující:

```
unxz [možnosti] [argumenty]
```

## Běžné možnosti
- `-k`, `--keep`: Zachová původní soubor po rozbalení.
- `-f`, `--force`: Přepíše existující soubory bez dotazu.
- `-v`, `--verbose`: Zobrazí podrobnosti o procesu rozbalování.

## Běžné příklady
Rozbalení souboru `soubor.xz`:

```
unxz soubor.xz
```

Zachování původního souboru při rozbalování:

```
unxz -k soubor.xz
```

Přepsání existujícího souboru bez dotazu:

```
unxz -f soubor.xz
```

Zobrazování podrobností během rozbalování:

```
unxz -v soubor.xz
```

## Tipy
- Před použitím příkazu `unxz` se ujistěte, že máte zálohu důležitých souborů, zejména pokud používáte možnost `-f`.
- Pokud často pracujete s komprimovanými soubory, zvažte použití skriptů pro automatizaci procesu rozbalování.
- Vždy zkontrolujte, zda máte nainstalovaný balíček `xz-utils`, který obsahuje příkaz `unxz`.