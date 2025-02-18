# [Český] Debian Almquist Shell (dash) printf použití: Formátování a výstup textu

## Přehled
Příkaz `printf` slouží k formátovanému výstupu textu na standardní výstup. Umožňuje uživatelům vytvářet strukturované a přehledné výstupy, které mohou obsahovat proměnné a specifikátory formátu.

## Použití
Základní syntaxe příkazu `printf` je následující:

```sh
printf [možnosti] [argumenty]
```

## Běžné možnosti
- `-v` : Umožňuje uložit výstup do proměnné místo na standardní výstup.
- `--help` : Zobrazí nápovědu k příkazu `printf`.
- `--version` : Zobrazí verzi příkazu `printf`.

## Běžné příklady
1. **Jednoduchý textový výstup:**
   ```sh
   printf "Ahoj, světe!\n"
   ```

2. **Formátování čísel:**
   ```sh
   printf "Číslo: %.2f\n" 3.14159
   ```

3. **Vypsání více hodnot:**
   ```sh
   printf "Jméno: %s, Věk: %d\n" "Jan" 30
   ```

4. **Uložení výstupu do proměnné:**
   ```sh
   printf -v my_var "Výstup: %s" "něco"
   echo "$my_var"
   ```

5. **Vytvoření tabulky:**
   ```sh
   printf "%-10s %-10s\n" "Jméno" "Věk"
   printf "%-10s %-10d\n" "Jan" 30
   printf "%-10s %-10d\n" "Petr" 25
   ```

## Tipy
- Používejte specifikátory formátu pro přesné řízení výstupu, jako je počet desetinných míst nebo šířka sloupců.
- Nezapomeňte na nový řádek (`\n`) na konci formátovacího řetězce, pokud chcete, aby výstup byl na nové řádce.
- Testujte příkazy v interaktivním shellu, abyste viděli, jak se formátování projevuje na výstupu.