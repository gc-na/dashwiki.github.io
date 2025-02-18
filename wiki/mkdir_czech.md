# [Český] Debian Almquist Shell (dash) mkdir použití: Vytváření adresářů

## Přehled
Příkaz `mkdir` slouží k vytváření nových adresářů v systému. Umožňuje uživatelům organizovat soubory do struktury adresářů.

## Použití
Základní syntaxe příkazu je následující:

```bash
mkdir [možnosti] [argumenty]
```

## Běžné možnosti
- `-p`: Vytvoří rodičovské adresáře podle potřeby.
- `-v`: Zobrazí podrobnosti o tom, co bylo vytvořeno.
- `--mode=MODE`: Nastaví oprávnění pro nový adresář.

## Běžné příklady
Vytvoření jednoduchého adresáře:

```bash
mkdir novy_adresar
```

Vytvoření více adresářů najednou:

```bash
mkdir adresar1 adresar2 adresar3
```

Vytvoření adresáře včetně rodičovských adresářů:

```bash
mkdir -p rodic/adresar
```

Zobrazení podrobností o vytvořeném adresáři:

```bash
mkdir -v novy_adresar
```

## Tipy
- Používejte možnost `-p`, pokud potřebujete vytvořit více úrovní adresářů najednou.
- Zkontrolujte oprávnění adresáře po jeho vytvoření, abyste zajistili, že jsou nastavena správně.
- Při vytváření adresářů s mezerami v názvu je dobré použít uvozovky, například: `mkdir "nový adresář"`.