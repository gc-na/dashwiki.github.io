# [Český] Debian Almquist Shell (dash) bg: [pozadí úloh]

## Přehled
Příkaz `bg` se používá v shellu pro pokračování pozastavených úloh na pozadí. Umožňuje uživatelům spustit procesy, které byly zastaveny, aniž by blokovaly terminál.

## Použití
Základní syntaxe příkazu je následující:

```bash
bg [možnosti] [argumenty]
```

## Běžné možnosti
- `job_id` - Identifikátor úlohy, kterou chcete poslat na pozadí. Může to být číslo úlohy nebo název procesu.
- `-n` - Nepoužívejte tuto možnost v `dash`, protože `bg` v `dash` nemá žádné specifické volby.

## Běžné příklady
1. **Pokračování poslední pozastavené úlohy na pozadí:**
   ```bash
   bg
   ```

2. **Pokračování konkrétní úlohy na pozadí:**
   Pokud máte pozastavenou úlohu s ID 1, můžete ji spustit na pozadí takto:
   ```bash
   bg %1
   ```

3. **Pokračování úlohy podle názvu:**
   Pokud máte úlohu, která byla pozastavena a chcete ji spustit na pozadí:
   ```bash
   bg my_process
   ```

## Tipy
- Před použitím příkazu `bg` se ujistěte, že úloha byla skutečně pozastavena pomocí příkazu `jobs`.
- Můžete kombinovat `bg` s příkazem `jobs` pro efektivní správu více úloh.
- Pokud potřebujete úlohu spustit na popředí, použijte příkaz `fg` místo `bg`.