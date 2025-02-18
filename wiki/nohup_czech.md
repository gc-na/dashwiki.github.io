# [Český] Debian Almquist Shell (dash) nohup použití: Spuštění příkazů bez ohledu na odhlášení

## Přehled
Příkaz `nohup` (no hang up) slouží k tomu, aby umožnil spouštět příkazy, které budou pokračovat v běhu i po odhlášení uživatele. To je užitečné pro dlouhotrvající úlohy, které by jinak byly přerušeny při odhlášení.

## Použití
Základní syntaxe příkazu `nohup` je následující:

```bash
nohup [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`, `--help`: Zobrazí nápovědu k příkazu.
- `-v`, `--version`: Zobrazí verzi příkazu `nohup`.
- `&`: Spustí příkaz na pozadí.

## Běžné příklady
1. Spuštění skriptu `myscript.sh` na pozadí, který bude pokračovat v běhu i po odhlášení:
   ```bash
   nohup ./myscript.sh &
   ```

2. Spuštění příkazu `ping`, který bude běžet i po odhlášení:
   ```bash
   nohup ping google.com &
   ```

3. Uložení výstupu příkazu do souboru `output.log`:
   ```bash
   nohup ./long_running_task > output.log &
   ```

4. Spuštění Python skriptu na pozadí:
   ```bash
   nohup python3 myscript.py &
   ```

## Tipy
- Vždy je dobré přesměrovat výstup do souboru, abyste mohli sledovat, co se děje, když příkaz běží na pozadí.
- Používejte `&` na konci příkazu, pokud chcete, aby se příkaz spustil na pozadí a vy mohli pokračovat v práci v terminálu.
- Pokud potřebujete zastavit běžící úlohu, můžete použít příkaz `kill` s PID (procesní identifikátor) úlohy.