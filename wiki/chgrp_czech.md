# [Český] Debian Almquist Shell (dash) chgrp: Změna skupinové příslušnosti souborů

## Přehled
Příkaz `chgrp` slouží ke změně skupinové příslušnosti souborů a adresářů v systému. Umožňuje uživatelům přiřadit soubory k jiné skupině, což může být užitečné pro správu oprávnění a sdílení souborů mezi uživateli.

## Použití
Základní syntaxe příkazu je následující:

```
chgrp [možnosti] [argumenty]
```

## Běžné možnosti
- `-R`: Rekurzivně změní skupinovou příslušnost všech souborů a podadresářů v daném adresáři.
- `-v`: Zobrazí podrobnosti o každé změně, kterou příkaz provádí.
- `--silent`: Potlačí výstup zpráv o úspěšných změnách.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `chgrp`:

1. Změna skupinové příslušnosti souboru `dokument.txt` na skupinu `nová_skupina`:
   ```bash
   chgrp nová_skupina dokument.txt
   ```

2. Rekurzivní změna skupinové příslušnosti všech souborů v adresáři `moje_adresář` na skupinu `sdílená_skupina`:
   ```bash
   chgrp -R sdílená_skupina moje_adresář
   ```

3. Zobrazení podrobností o změně skupinové příslušnosti souboru `obrázek.png` na skupinu `grafici`:
   ```bash
   chgrp -v grafici obrázek.png
   ```

## Tipy
- Před použitím příkazu `chgrp` se ujistěte, že máte potřebná oprávnění ke změně skupinové příslušnosti souborů.
- Používejte možnost `-R` s opatrností, zejména v případě, že měníte skupinovou příslušnost velkého množství souborů.
- Zkontrolujte aktuální skupinovou příslušnost souboru pomocí příkazu `ls -l`, abyste se ujistili, že změny byly provedeny správně.