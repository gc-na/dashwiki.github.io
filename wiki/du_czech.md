# [Český] Debian Almquist Shell (dash) du použití: Zobrazování velikosti souborů a adresářů

## Přehled
Příkaz `du` (disk usage) slouží k zobrazení velikosti souborů a adresářů v systému. Umožňuje uživatelům zjistit, kolik místa na disku jednotlivé soubory a složky zabírají.

## Použití
Základní syntaxe příkazu `du` je následující:

```
du [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Zobrazí velikosti v lidsky čitelném formátu (např. KB, MB).
- `-s`: Zobrazí pouze celkovou velikost pro každý argument.
- `-a`: Zobrazí velikosti pro všechny soubory, nejen pro adresáře.
- `-c`: Zobrazí celkovou velikost na konci výstupu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `du`:

1. Zobrazení velikosti aktuálního adresáře a jeho podadresářů:
   ```bash
   du
   ```

2. Zobrazení velikosti aktuálního adresáře v lidsky čitelném formátu:
   ```bash
   du -h
   ```

3. Zobrazení celkové velikosti konkrétního adresáře:
   ```bash
   du -sh /cesta/k/adresáři
   ```

4. Zobrazení velikosti všech souborů a adresářů v aktuálním adresáři:
   ```bash
   du -a
   ```

5. Zobrazení velikosti adresářů s celkovým součtem na konci:
   ```bash
   du -ch
   ```

## Tipy
- Používejte možnost `-h`, pokud chcete snadno porovnat velikosti souborů a adresářů.
- Pokud potřebujete zjistit, které soubory zabírají nejvíce místa, zkombinujte `du` s příkazem `sort`:
  ```bash
  du -ah | sort -rh | head -n 10
  ```
- Pravidelně kontrolujte velikosti adresářů, abyste se vyhnuli zaplnění disku.