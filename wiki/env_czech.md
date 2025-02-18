# [Český] Debian Almquist Shell (dash) env použití: Správa prostředí

## Přehled
Příkaz `env` se používá k zobrazení nebo nastavení environmentálních proměnných v shellu. Umožňuje spouštět příkazy s upraveným prostředím, což je užitečné pro testování nebo spouštění skriptů s různými nastaveními.

## Použití
Základní syntaxe příkazu `env` je následující:

```sh
env [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`: Spustí příkaz s prázdným prostředím, bez jakýchkoliv předchozích proměnných.
- `-u VAR`: Odstraní proměnnou `VAR` z prostředí před spuštěním příkazu.
- `VAR=value`: Nastaví proměnnou `VAR` na hodnotu `value` pro daný příkaz.

## Běžné příklady
1. Zobrazení všech environmentálních proměnných:
   ```sh
   env
   ```

2. Spuštění příkazu s prázdným prostředím:
   ```sh
   env -i bash
   ```

3. Nastavení proměnné a spuštění příkazu:
   ```sh
   env MY_VAR=hello ./my_script.sh
   ```

4. Odstranění proměnné před spuštěním příkazu:
   ```sh
   env -u MY_VAR ./my_script.sh
   ```

## Tipy
- Používejte `env` pro testování skriptů s různými nastaveními prostředí, abyste se ujistili, že fungují správně.
- Při používání `-i` buďte opatrní, protože odstraní všechny proměnné prostředí, což může ovlivnit chování příkazů.
- Můžete kombinovat více proměnných a příkazů v jednom příkazu `env`, což usnadňuje správu prostředí.