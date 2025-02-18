# [Debian] Debian Almquist Shell (dash) true: [vždy úspěšné provedení]

## Přehled
Příkaz `true` v shellu Debian Almquist (dash) je jednoduchý příkaz, který vždy vrací úspěšný stav (exit status 0). Je často používán v skriptech a automatizovaných úlohách, kde je potřeba zajistit, že se provede nějaká akce bez ohledu na okolnosti.

## Použití
Základní syntaxe příkazu `true` je následující:

```
true [options] [arguments]
```

## Běžné možnosti
Příkaz `true` nemá žádné specifické možnosti ani argumenty. Jeho hlavní funkcí je vrátit úspěšný stav.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `true`:

1. **Použití v podmínkovém příkazu**:
   ```sh
   if true; then
       echo "Toto se vždy vykoná."
   fi
   ```

2. **Vytvoření nekonečné smyčky**:
   ```sh
   while true; do
       echo "Toto se opakuje donekonečna."
       sleep 1
   done
   ```

3. **Zajištění úspěšného ukončení skriptu**:
   ```sh
   #!/bin/dash
   echo "Skript běží..."
   true
   echo "Skript skončil úspěšně."
   ```

## Tipy
- Používejte `true` v skriptech, kde potřebujete zajistit, že se nějaký blok kódu vykoná bez ohledu na předchozí chyby.
- Můžete jej kombinovat s příkazem `&&` pro provedení dalších příkazů pouze v případě úspěchu.
- `true` je užitečné při testování podmínek, kde chcete, aby se něco stalo bez ohledu na výsledek předchozího příkazu.