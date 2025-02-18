# [Český] Debian Almquist Shell (dash) uptime použití: Zobrazení doby běhu systému

## Přehled
Příkaz `uptime` v shellu dash zobrazuje, jak dlouho je systém spuštěn, kolik uživatelů je přihlášeno a průměrné zatížení systému za posledních 1, 5 a 15 minut. Tento příkaz je užitečný pro rychlé zhodnocení stavu systému.

## Použití
Základní syntaxe příkazu `uptime` je následující:

```
uptime [možnosti]
```

## Běžné možnosti
- `-p`: Zobrazí dobu běhu systému v přátelském formátu.
- `-s`: Zobrazí čas, kdy byl systém naposledy spuštěn.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `uptime`:

1. Základní příkaz pro zobrazení doby běhu systému:
   ```sh
   uptime
   ```

2. Zobrazení doby běhu v přátelském formátu:
   ```sh
   uptime -p
   ```

3. Zobrazení času posledního spuštění systému:
   ```sh
   uptime -s
   ```

## Tipy
- Používejte příkaz `uptime` pravidelně, abyste sledovali výkon a stabilitu vašeho systému.
- Kombinujte `uptime` s dalšími příkazy, jako je `top`, pro podrobnější analýzu zatížení systému.
- Pokud potřebujete informace o uživatelích, zkombinujte `uptime` s příkazem `who` pro zobrazení aktivních uživatelů.