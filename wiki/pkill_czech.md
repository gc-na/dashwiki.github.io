# [Debian] Debian Almquist Shell (dash) pkill použití: Ukončení procesů podle názvu

## Přehled
Příkaz `pkill` slouží k ukončení procesů na základě jejich názvu nebo jiných atributů. Umožňuje uživatelům efektivně spravovat běžící procesy bez nutnosti hledat jejich PID (identifikační číslo procesu).

## Použití
Základní syntaxe příkazu `pkill` je následující:

```bash
pkill [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`: Umožňuje vyhledávat podle celého příkazu, nikoli pouze podle názvu procesu.
- `-n`: Ukončí pouze nejnovější proces, který odpovídá zadaným kritériím.
- `-o`: Ukončí pouze nejstarší proces, který odpovídá zadaným kritériím.
- `-signal`: Určuje signál, který má být odeslán procesu (např. `-9` pro SIGKILL).

## Běžné příklady
1. Ukončení všech procesů s názvem `firefox`:
   ```bash
   pkill firefox
   ```

2. Ukončení všech procesů, které obsahují `python` v názvu příkazu:
   ```bash
   pkill -f python
   ```

3. Ukončení nejnovějšího procesu s názvem `ssh`:
   ```bash
   pkill -n ssh
   ```

4. Odeslání signálu SIGKILL (9) na všechny procesy s názvem `gedit`:
   ```bash
   pkill -9 gedit
   ```

## Tipy
- Před použitím příkazu `pkill` je dobré ověřit, které procesy budou ukončeny, například pomocí `pgrep` s podobnými argumenty.
- Používejte `pkill` opatrně, zejména s možností `-9`, protože to může způsobit ztrátu neuložených dat v aplikacích.
- Pokud je to možné, zkuste nejprve použít méně drsné signály (např. `-15` pro SIGTERM) před použitím SIGKILL.