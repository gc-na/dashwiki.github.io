# [Český] Debian Almquist Shell (dash) pidstat použití: Monitorování statistiky procesů

## Přehled
Příkaz `pidstat` slouží k monitorování výkonu procesů v systému. Umožňuje uživatelům sledovat různé statistiky, jako je využití CPU, paměti a další metriky pro jednotlivé procesy, což je užitečné pro diagnostiku a optimalizaci výkonu.

## Použití
Základní syntaxe příkazu je následující:

```bash
pidstat [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Zobrazí hlavičku s názvy sloupců.
- `-r`: Zobrazí statistiky využití paměti.
- `-u`: Zobrazí statistiky využití CPU.
- `-p <pid>`: Sleduje specifický proces podle jeho PID.
- `-t`: Zobrazí informace o vláknech.

## Běžné příklady
1. Zobrazení využití CPU pro všechny procesy:
   ```bash
   pidstat -u
   ```

2. Zobrazení využití paměti pro všechny procesy:
   ```bash
   pidstat -r
   ```

3. Sledování specifického procesu podle jeho PID (např. PID 1234):
   ```bash
   pidstat -p 1234
   ```

4. Zobrazení statistik pro všechny procesy v intervalech 2 sekundy:
   ```bash
   pidstat 2
   ```

5. Zobrazení statistik pro vlákna:
   ```bash
   pidstat -t
   ```

## Tipy
- Používejte příkaz `pidstat` v kombinaci s dalšími nástroji, jako je `grep`, pro filtrování výstupu podle konkrétních procesů.
- Pravidelně sledujte procesy s vysokým využitím CPU nebo paměti, abyste identifikovali potenciální problémy.
- Využijte možnost `-h` pro lepší čitelnost výstupu, zejména pokud pracujete s velkým množstvím dat.