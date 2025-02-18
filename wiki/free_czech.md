# [Český] Debian Almquist Shell (dash) free příkaz: zobrazení informací o paměti

## Přehled
Příkaz `free` slouží k zobrazení informací o využití paměti v systému. Ukazuje, kolik paměti je aktuálně využito, kolik je volné a další důležité statistiky, které pomáhají uživatelům sledovat výkon systému.

## Použití
Základní syntaxe příkazu `free` je následující:

```
free [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Zobrazí hodnoty v lidsky čitelném formátu (např. MB, GB).
- `-m`: Zobrazí hodnoty v megabajtech.
- `-g`: Zobrazí hodnoty v gigabajtech.
- `-s [sekundy]`: Aktualizuje výstup každé [sekundy] (např. `-s 5` pro každých 5 sekund).
- `-t`: Zobrazí celkovou paměť (součet fyzické a swap paměti).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `free`:

1. Základní zobrazení informací o paměti:
   ```bash
   free
   ```

2. Zobrazení informací v lidsky čitelném formátu:
   ```bash
   free -h
   ```

3. Zobrazení paměti v megabajtech:
   ```bash
   free -m
   ```

4. Aktualizace informací každých 5 sekund:
   ```bash
   free -s 5
   ```

5. Zobrazení celkové paměti:
   ```bash
   free -t
   ```

## Tipy
- Používejte možnost `-h`, abyste snadno porozuměli hodnotám paměti, zejména pokud pracujete s většími systémy.
- Pokud potřebujete sledovat paměť v reálném čase, kombinujte `free` s příkazem `watch`:
   ```bash
   watch free -h
   ```
- Pravidelně kontrolujte využití paměti, abyste předešli problémům s výkonem systému.