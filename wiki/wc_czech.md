# [Český] Debian Almquist Shell (dash) wc použití: Počítání řádků, slov a znaků

## Přehled
Příkaz `wc` (word count) slouží k počítání řádků, slov a znaků v textových souborech. Tento příkaz je užitečný pro rychlé zjištění velikosti souboru nebo pro analýzu obsahu.

## Použití
Základní syntaxe příkazu je následující:

```
wc [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Počítá pouze řádky.
- `-w`: Počítá pouze slova.
- `-c`: Počítá pouze znaky.
- `-m`: Počítá pouze znaky (včetně multibyte znaků).
- `-L`: Zobrazí délku nejdelšího řádku.

## Běžné příklady
1. Počítání řádků, slov a znaků v souboru `soubor.txt`:
   ```bash
   wc soubor.txt
   ```

2. Počítání pouze řádků:
   ```bash
   wc -l soubor.txt
   ```

3. Počítání pouze slov:
   ```bash
   wc -w soubor.txt
   ```

4. Počítání pouze znaků:
   ```bash
   wc -c soubor.txt
   ```

5. Počítání délky nejdelšího řádku:
   ```bash
   wc -L soubor.txt
   ```

## Tipy
- Pokud chcete počítat více souborů najednou, stačí je uvést za sebe:
  ```bash
  wc soubor1.txt soubor2.txt
  ```
- Pro zobrazení pouze počtu řádků můžete použít příkaz v kombinaci s dalšími příkazy, například:
  ```bash
  cat soubor.txt | wc -l
  ```
- Příkaz `wc` je užitečný v kombinaci s dalšími příkazy v shellu, například `grep`, pro analýzu výstupu.