# [Český] Debian Almquist Shell (dash) ls Použití: Zobrazit obsah adresáře

## Přehled
Příkaz `ls` slouží k zobrazení obsahu adresáře. Umožňuje uživatelům vidět soubory a podadresáře v aktuálním nebo zvoleném adresáři.

## Použití
Základní syntaxe příkazu `ls` je následující:

```bash
ls [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Zobrazí podrobný seznam souborů včetně oprávnění, vlastníka, velikosti a data poslední změny.
- `-a`: Zobrazí všechny soubory, včetně skrytých (ty, které začínají tečkou).
- `-h`: Zobrazí velikosti souborů v lidsky čitelném formátu (např. KB, MB).
- `-R`: Rekurzivně zobrazí obsah všech podadresářů.
- `-t`: Seřadí soubory podle data poslední změny, od nejnovějšího po nejstarší.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `ls`:

1. Zobrazit všechny soubory v aktuálním adresáři:
   ```bash
   ls
   ```

2. Zobrazit podrobný seznam souborů:
   ```bash
   ls -l
   ```

3. Zobrazit všechny soubory, včetně skrytých:
   ```bash
   ls -a
   ```

4. Zobrazit soubory s lidsky čitelnými velikostmi:
   ```bash
   ls -lh
   ```

5. Rekurzivně zobrazit obsah adresáře:
   ```bash
   ls -R
   ```

6. Seřadit soubory podle data poslední změny:
   ```bash
   ls -lt
   ```

## Tipy
- Používejte kombinace možností pro přizpůsobení výstupu podle svých potřeb, například `ls -la` pro zobrazení všech souborů v podrobném formátu.
- Pokud chcete zobrazit soubory v určitém adresáři, můžete přidat cestu k adresáři jako argument, například `ls /cesta/k/adresáři`.
- Pro rychlé zobrazení obsahu adresáře můžete použít alias, například `alias ll='ls -l'`, což vám umožní rychleji získat podrobný seznam souborů.