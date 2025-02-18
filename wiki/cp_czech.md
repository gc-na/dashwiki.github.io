# [Český] Debian Almquist Shell (dash) cp použití: Kopírování souborů a adresářů

## Přehled
Příkaz `cp` slouží k kopírování souborů a adresářů v systému. Umožňuje uživatelům snadno vytvářet kopie souborů na stejném nebo jiném místě v souborovém systému.

## Použití
Základní syntaxe příkazu `cp` je následující:

```bash
cp [možnosti] [argumenty]
```

## Běžné možnosti
- `-r`: Rekurzivně kopíruje adresáře a jejich obsah.
- `-i`: Interaktivní režim, který se ptá před přepsáním existujícího souboru.
- `-u`: Kopíruje pouze, pokud je zdrojový soubor novější než cílový soubor nebo pokud cílový soubor neexistuje.
- `-v`: Zobrazí podrobnosti o tom, co se kopíruje (verbose).

## Běžné příklady
Kopírování souboru `soubor.txt` do cílového adresáře `adresar/`:

```bash
cp soubor.txt adresar/
```

Kopírování adresáře `moje_adresar` a jeho obsahu do `novy_adresar`:

```bash
cp -r moje_adresar novy_adresar
```

Kopírování souboru s potvrzením před přepsáním:

```bash
cp -i soubor.txt adresar/
```

Kopírování pouze novějších souborů:

```bash
cp -u soubor.txt adresar/
```

## Tipy
- Před použitím příkazu `cp` se ujistěte, že máte správná oprávnění pro čtení zdrojového souboru a zápis do cílového umístění.
- Používejte možnost `-v`, abyste měli přehled o tom, co se kopíruje, zejména při práci s více soubory.
- Při kopírování důležitých souborů zvažte použití možnosti `-i`, abyste se vyhnuli nechtěnému přepsání.