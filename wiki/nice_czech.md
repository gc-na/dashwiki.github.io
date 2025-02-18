# [Český] Debian Almquist Shell (dash) nice použití: Nastavení priority procesů

## Přehled
Příkaz `nice` se používá k nastavení priority procesů při jejich spuštění. Umožňuje uživatelům spouštět programy s nižší nebo vyšší prioritou, což může být užitečné pro optimalizaci výkonu systému a zajištění, že důležité úlohy mají dostatek systémových prostředků.

## Použití
Základní syntaxe příkazu `nice` je následující:

```bash
nice [možnosti] [argumenty]
```

## Běžné možnosti
- `-n, --adjustment=N`: Nastaví hodnotu priority na N. Výchozí hodnota je 10, což znamená, že proces bude mít nižší prioritu.
- `-h, --help`: Zobrazí nápovědu k příkazu.
- `--version`: Zobrazí verzi příkazu.

## Běžné příklady
1. Spuštění programu `my_script.sh` s nižší prioritou (10):

   ```bash
   nice -n 10 ./my_script.sh
   ```

2. Spuštění programu `backup.sh` s vyšší prioritou (-5):

   ```bash
   nice -n -5 ./backup.sh
   ```

3. Zobrazení aktuálního nastavení priority pro běžící proces:

   ```bash
   nice -n 0 ps
   ```

4. Spuštění příkazu `make` s výchozí prioritou:

   ```bash
   nice make
   ```

## Tipy
- Používejte `nice` pro méně důležité úlohy, aby se zajistilo, že důležitější procesy nebudou zpomalovány.
- Mějte na paměti, že pouze uživatel s oprávněním může zvyšovat prioritu procesů (tj. nastavovat záporné hodnoty).
- Pro sledování aktuálních priorit běžících procesů můžete použít příkaz `top` nebo `htop`.