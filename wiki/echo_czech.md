# [Český] Debian Almquist Shell (dash) echo použití: Zobrazí text na standardním výstupu

## Přehled
Příkaz `echo` slouží k zobrazení textu nebo proměnných na standardním výstupu. Je to užitečný nástroj pro zobrazování zpráv, hodnot proměnných nebo pro formátování výstupu skriptů.

## Použití
Základní syntaxe příkazu `echo` je následující:

```sh
echo [možnosti] [argumenty]
```

## Běžné možnosti
- `-n`: Nezobrazí nový řádek na konci výstupu.
- `-e`: Aktivuje interpretaci escape sekvencí (např. `\n` pro nový řádek).
- `-E`: Deaktivuje interpretaci escape sekvencí (toto je výchozí chování).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `echo`:

1. Základní zobrazení textu:
   ```sh
   echo "Ahoj, světe!"
   ```

2. Zobrazení proměnné:
   ```sh
   jmeno="Jan"
   echo "Moje jméno je $jmeno."
   ```

3. Zobrazení textu bez nového řádku:
   ```sh
   echo -n "Toto je text bez nového řádku."
   ```

4. Použití escape sekvencí:
   ```sh
   echo -e "První řádek\nDruhý řádek"
   ```

5. Zobrazení cesty k aktuálnímu adresáři:
   ```sh
   echo "Aktuální adresář je: $(pwd)"
   ```

## Tipy
- Používejte `-n`, pokud chcete, aby výstup pokračoval na stejném řádku.
- Pokud potřebujete zobrazit speciální znaky (např. `$`), použijte jednoduché uvozovky (`'`) místo dvojitých (`"`).
- Příkaz `echo` je často používán ve skriptech pro ladění, kde můžete zobrazit hodnoty proměnných v různých bodech skriptu.