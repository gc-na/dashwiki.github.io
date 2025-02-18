# [Český] Debian Almquist Shell (dash) dirname použití: Získání názvu adresáře souboru

## Přehled
Příkaz `dirname` slouží k extrakci názvu adresáře z cesty k souboru. V podstatě vrací část cesty, která vede k souboru, bez samotného názvu souboru.

## Použití
Základní syntaxe příkazu je následující:

```
dirname [možnosti] [argumenty]
```

## Běžné možnosti
- `-z`: Vytiskne výstup jako nulou oddělený seznam, což je užitečné pro zpracování souborů obsahujících mezery.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `dirname`:

1. Získání názvu adresáře z cesty:
   ```sh
   dirname /home/uzivatel/dokumenty/soubor.txt
   ```
   Výstup: `/home/uzivatel/dokumenty`

2. Získání názvu adresáře z relativní cesty:
   ```sh
   dirname ./dokumenty/soubor.txt
   ```
   Výstup: `./dokumenty`

3. Použití s nulou odděleným výstupem:
   ```sh
   dirname -z /home/uzivatel/dokumenty/soubor.txt
   ```
   (Výstup bude nulou oddělený, což může být užitečné pro skripty.)

## Tipy
- Pokud potřebujete zpracovat více souborů najednou, můžete použít příkaz `xargs` k předání seznamu souborů příkazu `dirname`.
- Při práci s cestami, které obsahují mezery, je dobré citovat cesty, aby se předešlo chybám.
- `dirname` je užitečný v skriptech pro manipulaci s cestami a organizaci souborů.