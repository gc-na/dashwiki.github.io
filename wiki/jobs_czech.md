# [Český] Debian Almquist Shell (dash) jobs použití: Zobrazování běžících úloh

## Přehled
Příkaz `jobs` v shellu dash slouží k zobrazení seznamu úloh, které běží na pozadí nebo jsou zastavené v aktuálním shellovém sezení. Umožňuje uživatelům sledovat stav těchto úloh a usnadňuje jejich správu.

## Použití
Základní syntaxe příkazu je následující:

```
jobs [options] [arguments]
```

## Běžné možnosti
- `-l`: Zobrazí PID (identifikační číslo procesu) každé úlohy.
- `-n`: Zobrazí pouze úlohy, které byly změněny od posledního volání příkazu `jobs`.
- `-p`: Zobrazí pouze PID úloh.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `jobs`:

1. Zobrazení všech běžících a zastavených úloh:
   ```sh
   jobs
   ```

2. Zobrazení úloh s PID:
   ```sh
   jobs -l
   ```

3. Zobrazení pouze úloh, které se změnily od posledního zobrazení:
   ```sh
   jobs -n
   ```

4. Zobrazení pouze PID úloh:
   ```sh
   jobs -p
   ```

## Tipy
- Používejte příkaz `jobs` pravidelně, abyste měli přehled o běžících úlohách a mohli je efektivně spravovat.
- Pokud potřebujete pozastavit nebo ukončit úlohu, můžete použít příkazy `fg` (přepnout na popředí) nebo `bg` (pokračovat na pozadí) ve spojení s číslem úlohy, které získáte pomocí `jobs`.
- Při práci s více úlohami si dávejte pozor na jejich stavy, abyste předešli ztrátě dat nebo zablokování procesů.