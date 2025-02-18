# [Český] Debian Almquist Shell (dash) rmdir: Odstranění prázdných adresářů

## Přehled
Příkaz `rmdir` slouží k odstranění prázdných adresářů. Pokud se pokusíte odstranit adresář, který obsahuje soubory nebo další adresáře, příkaz selže.

## Použití
Základní syntaxe příkazu je následující:

```
rmdir [možnosti] [argumenty]
```

## Běžné možnosti
- `--ignore-fail-on-non-empty`: Tato možnost způsobí, že příkaz nebude hlásit chybu, pokud se pokusíte odstranit neprázdný adresář.
- `--verbose`: Zobrazí podrobnosti o každém odstraněném adresáři.

## Běžné příklady
Odstranění prázdného adresáře:

```bash
rmdir /cesta/k/adresari
```

Odstranění více prázdných adresářů najednou:

```bash
rmdir /cesta/k/adresari1 /cesta/k/adresari2
```

Použití možnosti `--verbose` pro zobrazení informací:

```bash
rmdir --verbose /cesta/k/adresari
```

## Tipy
- Před použitím příkazu `rmdir` se ujistěte, že adresář je skutečně prázdný, jinak příkaz selže.
- Pokud potřebujete odstranit adresář, který obsahuje soubory, zvažte použití příkazu `rm -r` místo `rmdir`.
- Vždy je dobré zálohovat důležité soubory před jejich odstraněním.