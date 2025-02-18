# [Český] Debian Almquist Shell (dash) netstat použití: Zobrazování síťových připojení

## Přehled
Příkaz `netstat` slouží k zobrazení aktivních síťových připojení, směrovacích tabulek a různých statistik o síti. Umožňuje uživatelům sledovat, jaké porty jsou otevřené a jaká spojení jsou navázána na jejich systému.

## Použití
Základní syntaxe příkazu `netstat` je následující:

```bash
netstat [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechna připojení a naslouchající porty.
- `-t`: Zobrazí pouze TCP připojení.
- `-u`: Zobrazí pouze UDP připojení.
- `-n`: Zobrazí adresy a porty v numerickém formátu místo pokusů o rozlišení názvů.
- `-l`: Zobrazí pouze naslouchající porty.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `netstat`:

1. Zobrazení všech aktivních připojení:
   ```bash
   netstat -a
   ```

2. Zobrazení pouze TCP připojení:
   ```bash
   netstat -t
   ```

3. Zobrazení naslouchajících portů:
   ```bash
   netstat -l
   ```

4. Zobrazení připojení s numerickými adresami:
   ```bash
   netstat -n
   ```

5. Zobrazení UDP připojení:
   ```bash
   netstat -u
   ```

## Tipy
- Používejte kombinaci možností pro podrobnější výstup, například `netstat -tunl` pro zobrazení všech naslouchajících TCP a UDP připojení v numerickém formátu.
- Pravidelně kontrolujte otevřené porty, abyste zajistili bezpečnost vašeho systému.
- Můžete také použít příkaz `grep` pro filtrování výsledků, například `netstat -a | grep :80` pro zobrazení připojení na portu 80.