# [Debian] Debian Almquist Shell (dash) renice: Změna priority běžících procesů

## Přehled
Příkaz `renice` slouží ke změně priority běžících procesů v systému. Pomocí tohoto příkazu můžete upravit hodnotu nice, což ovlivňuje, jaký čas CPU bude procesům přidělen. Nižší hodnota nice znamená vyšší prioritu.

## Použití
Základní syntaxe příkazu je následující:

```
renice [options] [arguments]
```

## Běžné možnosti
- `-n`, `--priority`: Určuje novou hodnotu nice. Může být jak kladná, tak záporná.
- `-p`, `--pid`: Určuje ID procesu, jehož prioritu chcete změnit.
- `-g`, `--pgrp`: Změní prioritu všech procesů v dané skupině.
- `-u`, `--user`: Změní prioritu všech procesů patřících danému uživateli.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `renice`:

1. Změna priority procesu s ID 1234 na 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Změna priority všech procesů patřících uživateli "john" na 5:
   ```bash
   renice -n 5 -u john
   ```

3. Změna priority skupiny procesů s ID 5678 na -5:
   ```bash
   renice -n -5 -g 5678
   ```

4. Získání aktuální priority procesu s ID 1234:
   ```bash
   ps -o pid,nice -p 1234
   ```

## Tipy
- Při používání `renice` buďte opatrní, protože zvyšování priority procesů může ovlivnit výkon systému.
- Používejte `renice` s oprávněními superuživatele (root), pokud se pokoušíte změnit prioritu procesů, které patří jiným uživatelům.
- Mějte na paměti, že příkaz `renice` může být použit pouze na běžící procesy; pro nové procesy použijte příkaz `nice`.