# [Český] Debian Almquist Shell (dash) iotop použití: Monitorování diskové aktivity

## Přehled
Příkaz `iotop` slouží k monitorování diskové aktivity procesů v reálném čase. Umožňuje uživatelům sledovat, které procesy využívají diskové vstupy a výstupy, což je užitečné pro diagnostiku výkonu systému.

## Použití
Základní syntaxe příkazu je následující:

```
iotop [možnosti] [argumenty]
```

## Běžné možnosti
- `-o`, `--only`: Zobrazí pouze procesy, které v současnosti generují I/O.
- `-b`, `--batch`: Spustí iotop v dávkovém režimu, což je užitečné pro logování.
- `-d`, `--delay`: Nastaví zpoždění mezi aktualizacemi v sekundách (výchozí je 1 sekunda).
- `-p`, `--pid`: Sleduje pouze procesy s daným PID.

## Běžné příklady
1. Základní spuštění iotop:
   ```bash
   iotop
   ```

2. Zobrazení pouze procesů generujících I/O:
   ```bash
   iotop -o
   ```

3. Spuštění iotop v dávkovém režimu s 2 sekundovým zpožděním:
   ```bash
   iotop -b -d 2
   ```

4. Sledování specifického procesu podle PID:
   ```bash
   iotop -p 1234
   ```

## Tipy
- Používejte `iotop` s právy superuživatele, abyste viděli všechny procesy, protože některé z nich mohou být skryté pro běžné uživatele.
- Pokud chcete logovat výstup do souboru, můžete použít příkaz `iotop -b -d 1 > iotop_log.txt`.
- Sledujte procesy s vysokou hodnotou I/O, abyste identifikovali potenciální problémy s výkonem.