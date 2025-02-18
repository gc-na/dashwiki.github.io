# [Český] Debian Almquist Shell (dash) pwd použití: Zobrazí aktuální pracovní adresář

## Přehled
Příkaz `pwd` (print working directory) slouží k zobrazení aktuálního pracovního adresáře v terminálu. Tento příkaz je užitečný pro ověření, kde se nacházíte v hierarchii souborového systému.

## Použití
Základní syntaxe příkazu je následující:

```
pwd [možnosti]
```

## Běžné možnosti
- `-L`: Zobrazí logickou cestu k aktuálnímu pracovnímu adresáři.
- `-P`: Zobrazí fyzickou cestu k aktuálnímu pracovnímu adresáři, což znamená, že se ignorují symbolické odkazy.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `pwd`:

1. Zobrazení aktuálního pracovního adresáře:
   ```bash
   pwd
   ```

2. Zobrazení fyzické cesty k aktuálnímu pracovnímu adresáři:
   ```bash
   pwd -P
   ```

3. Zobrazení logické cesty k aktuálnímu pracovnímu adresáři:
   ```bash
   pwd -L
   ```

## Tipy
- Používejte `pwd` pravidelně, abyste měli přehled o tom, kde se nacházíte v systému.
- Pokud pracujete s více terminály, můžete použít `pwd` k rychlému ověření aktuálního adresáře v každém z nich.
- Při skriptování může být užitečné uložit výstup `pwd` do proměnné pro další zpracování.