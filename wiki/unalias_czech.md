# [Český] Debian Almquist Shell (dash) unalias: Odstranění aliasů

## Přehled
Příkaz `unalias` slouží k odstranění aliasů, které byly dříve definovány v shellu. Alias je zjednodušený příkaz, který uživatelé vytvářejí pro usnadnění opakovaného používání příkazů.

## Použití
Základní syntaxe příkazu `unalias` je následující:

```
unalias [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Odstraní všechny definované aliasy.
- `-m`: Umožňuje odstranit aliasy, které odpovídají zadanému vzoru.

## Běžné příklady
1. Odstranění konkrétního aliasu:
   ```sh
   unalias ll
   ```

2. Odstranění všech aliasů:
   ```sh
   unalias -a
   ```

3. Odstranění aliasu podle vzoru:
   ```sh
   unalias -m 'l*'
   ```

## Tipy
- Před odstraněním aliasu se ujistěte, že víte, jaké aliasy máte definované. Můžete použít příkaz `alias` pro zobrazení všech aktuálních aliasů.
- Pokud potřebujete dočasně použít alias, můžete použít příkaz `unalias` v rámci skriptu nebo příkazového řádku, abyste se vyhnuli konfliktům.