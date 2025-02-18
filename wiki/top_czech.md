# [Český] Debian Almquist Shell (dash) top příkaz: Zobrazit běžící procesy

## Přehled
Příkaz `top` slouží k zobrazení aktuálně běžících procesů v systému. Umožňuje uživatelům sledovat využití CPU, paměti a další důležité informace o procesech v reálném čase.

## Použití
Základní syntaxe příkazu `top` je následující:

```
top [možnosti] [argumenty]
```

## Běžné možnosti
- `-d <sekundy>`: Nastaví interval aktualizace výstupu v sekundách.
- `-n <číslo>`: Určuje počet iterací, které se mají provést, než se příkaz ukončí.
- `-u <uživatel>`: Filtruje procesy podle specifikovaného uživatele.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `top`:

1. Spuštění příkazu `top` s výchozími nastaveními:
   ```bash
   top
   ```

2. Zobrazení procesů s aktualizací každé 5 sekundy:
   ```bash
   top -d 5
   ```

3. Zobrazení procesů pouze pro konkrétního uživatele:
   ```bash
   top -u username
   ```

4. Spuštění `top` a omezení na 10 iterací:
   ```bash
   top -n 10
   ```

## Tipy
- Pro zastavení příkazu `top` stiskněte klávesu `q`.
- Můžete použít klávesy `h` pro zobrazení nápovědy přímo v rozhraní `top`.
- Uložení výstupu do souboru můžete provést pomocí přesměrování, například:
  ```bash
  top -b -n 1 > top_output.txt
  ```
  Tímto způsobem můžete získat snapshot běžících procesů a uložit ho do souboru.