# [Český] Debian Almquist Shell (dash) pgrep použití: Hledání procesů podle názvu

## Přehled
Příkaz `pgrep` slouží k vyhledávání procesů běžících v systému podle jejich názvů nebo dalších kritérií. Umožňuje uživatelům snadno zjistit, které procesy jsou aktivní a splňují zadané podmínky.

## Použití
Základní syntaxe příkazu `pgrep` je následující:

```
pgrep [možnosti] [argumenty]
```

## Běžné možnosti
- `-u, --user <uživatel>`: Hledá procesy běžící pod specifikovaným uživatelským jménem nebo ID.
- `-f, --full`: Hledá podle celého příkazu, nikoli pouze podle názvu procesu.
- `-n, --newest`: Vrátí nejnovější proces, který odpovídá zadaným kritériím.
- `-o, --oldest`: Vrátí nejstarší proces, který odpovídá zadaným kritériím.

## Běžné příklady
- Hledání procesů podle názvu:
    ```bash
    pgrep bash
    ```
- Hledání procesů běžících pod konkrétním uživatelským jménem:
    ```bash
    pgrep -u john
    ```
- Hledání procesů podle celého příkazu:
    ```bash
    pgrep -f "python script.py"
    ```
- Získání nejnovějšího procesu podle názvu:
    ```bash
    pgrep -n ssh
    ```

## Tipy
- Používejte `pgrep` v kombinaci s příkazem `kill` pro efektivní ukončení procesů: 
    ```bash
    kill $(pgrep my_process)
    ```
- Pokud potřebujete více informací o procesech, zkombinujte `pgrep` s příkazem `ps`:
    ```bash
    ps -p $(pgrep my_process)
    ```
- Pro zúžení výsledků můžete kombinovat více možností, například hledání podle uživatele a názvu procesu současně.