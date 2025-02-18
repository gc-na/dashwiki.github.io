# [Český] Debian Almquist Shell (dash) kill použití: Ukončení procesů

## Přehled
Příkaz `kill` slouží k ukončení běžících procesů v systému. Umožňuje uživatelům posílat signály procesům, což může zahrnovat požadavek na jejich ukončení nebo jinou akci.

## Použití
Základní syntaxe příkazu je následující:

```bash
kill [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Vypíše seznam dostupných signálů.
- `-s SIGNÁL`: Určuje signál, který má být odeslán (např. `TERM`, `KILL`).
- `-n ČÍSLO`: Odesílá signál podle jeho čísla.

## Běžné příklady
1. Ukončení procesu podle jeho PID (identifikátor procesu):
   ```bash
   kill 1234
   ```

2. Odeslání signálu `SIGTERM` (standardní signál pro ukončení):
   ```bash
   kill -s TERM 1234
   ```

3. Odeslání signálu `SIGKILL`, který okamžitě ukončí proces:
   ```bash
   kill -s KILL 1234
   ```

4. Vypisování dostupných signálů:
   ```bash
   kill -l
   ```

5. Odeslání signálu podle jeho čísla (např. signál 9 pro `SIGKILL`):
   ```bash
   kill -n 9 1234
   ```

## Tipy
- Před použitím příkazu `kill` zjistěte, které procesy běží, pomocí příkazu `ps` nebo `top`.
- Používejte `SIGTERM` před `SIGKILL`, protože `SIGTERM` dává procesu šanci na řádné ukončení.
- Pokud potřebujete ukončit více procesů najednou, můžete zadat více PID oddělených mezerou:
  ```bash
  kill 1234 5678
  ```