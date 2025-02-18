# [Český] Debian Almquist Shell (dash) wait <Použití>: čekání na dokončení procesů

## Přehled
Příkaz `wait` v shellu dash slouží k pozastavení vykonávání skriptu, dokud nedokončí všechny podřízené procesy. Tento příkaz je užitečný, když potřebujete počkat na dokončení určitého procesu, než budete pokračovat s dalšími příkazy.

## Použití
Základní syntaxe příkazu `wait` je následující:

```bash
wait [options] [arguments]
```

## Běžné možnosti
- `PID` - Číslo procesu, na který chcete čekat. Pokud není uvedeno, `wait` čeká na všechny podřízené procesy.

## Běžné příklady

1. **Čekání na všechny podřízené procesy:**
   ```bash
   sleep 5 &
   sleep 3 &
   wait
   echo "Všechny procesy dokončeny."
   ```

2. **Čekání na konkrétní proces:**
   ```bash
   sleep 5 &
   PID=$!
   echo "Čekám na proces s PID: $PID"
   wait $PID
   echo "Proces s PID: $PID dokončen."
   ```

3. **Použití s více procesy:**
   ```bash
   (sleep 2; echo "Proces 1 dokončen.") &
   (sleep 4; echo "Proces 2 dokončen.") &
   wait
   echo "Všechny procesy byly dokončeny."
   ```

## Tipy
- Pokud používáte `wait` bez argumentů, ujistěte se, že máte spuštěné podřízené procesy, jinak příkaz okamžitě skončí.
- Uložení PID podřízeného procesu do proměnné vám umožní čekat na konkrétní proces a lépe řídit tok skriptu.
- Při použití `wait` v skriptech, které spouští více procesů současně, může pomoci efektivně řídit jejich dokončení a výstupy.