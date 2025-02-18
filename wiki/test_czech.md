# [Český] Debian Almquist Shell (dash) test použití: Ověření podmínek

## Přehled
Příkaz `test` se používá k vyhodnocení podmínek v shell skriptech. Umožňuje provádět logické a aritmetické testy, což je užitečné pro rozhodování v rámci skriptů.

## Použití
Základní syntaxe příkazu `test` je následující:

```sh
test [možnosti] [argumenty]
```

## Běžné možnosti
- `-e [soubor]`: Ověří, zda soubor existuje.
- `-d [adresář]`: Ověří, zda je zadaný argument adresář.
- `-f [soubor]`: Ověří, zda je zadaný argument běžný soubor.
- `-z [řetězec]`: Ověří, zda je řetězec prázdný.
- `-n [řetězec]`: Ověří, zda je řetězec neprázdný.
- `[řetězec1] = [řetězec2]`: Ověří, zda jsou dva řetězce shodné.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `test`:

1. Ověření existence souboru:
   ```sh
   test -e soubor.txt && echo "Soubor existuje."
   ```

2. Ověření, zda je zadaný argument adresář:
   ```sh
   test -d /cesta/k/adresari && echo "Je to adresář."
   ```

3. Ověření, zda je soubor běžný soubor:
   ```sh
   test -f soubor.txt && echo "Je to běžný soubor."
   ```

4. Ověření, zda je řetězec prázdný:
   ```sh
   test -z "$RETEZEC" && echo "Řetězec je prázdný."
   ```

5. Ověření shody dvou řetězců:
   ```sh
   test "$RETEZEC1" = "$RETEZEC2" && echo "Řetězce jsou shodné."
   ```

## Tipy
- Používejte `&&` pro spojení příkazů, abyste provedli další akce pouze v případě, že test byl úspěšný.
- Mějte na paměti, že příkaz `test` vrací status 0 při úspěchu a 1 při neúspěchu, což můžete využít v podmínkových příkazech.
- Pro lepší čitelnost můžete použít zkrácenou syntaxi `[` a `]`, např. `[ -e soubor.txt ]`.