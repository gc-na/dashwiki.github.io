# [Český] Debian Almquist Shell (dash) uname použití: Získání informací o systému

## Přehled
Příkaz `uname` slouží k zobrazení základních informací o operačním systému a jádru, na kterém běží. Může poskytnout informace jako název jádra, verzi, architekturu a další detaily, které jsou užitečné pro diagnostiku a správu systému.

## Použití
Základní syntaxe příkazu `uname` je následující:

```
uname [možnosti]
```

## Běžné možnosti
- `-a`: Zobrazí všechny dostupné informace o systému.
- `-s`: Zobrazí název jádra.
- `-n`: Zobrazí název hostitele.
- `-r`: Zobrazí verzi jádra.
- `-v`: Zobrazí datum a čas kompilace jádra.
- `-m`: Zobrazí architekturu stroje.
- `-o`: Zobrazí název operačního systému.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `uname`:

1. Zobrazení všech dostupných informací o systému:
   ```sh
   uname -a
   ```

2. Zobrazení názvu jádra:
   ```sh
   uname -s
   ```

3. Zobrazení verze jádra:
   ```sh
   uname -r
   ```

4. Zobrazení architektury stroje:
   ```sh
   uname -m
   ```

5. Zobrazení názvu operačního systému:
   ```sh
   uname -o
   ```

## Tipy
- Používejte možnost `-a`, pokud potřebujete rychlý přehled o systému, protože zobrazuje všechny informace najednou.
- Příkaz `uname` je užitečný při skriptování, kdy potřebujete zjistit specifické informace o systému pro další zpracování.
- Mějte na paměti, že některé možnosti nemusí být dostupné na všech systémech, proto je dobré zkontrolovat dokumentaci pro konkrétní distribuci.