# [Český] Debian Almquist Shell (dash) id použití: Zobrazí informace o uživatelském ID

## Přehled
Příkaz `id` slouží k zobrazení informací o uživatelském ID a skupinách, do kterých uživatel patří. Tento příkaz je užitečný pro zjištění, jaké oprávnění má aktuální uživatel nebo jiný uživatel v systému.

## Použití
Základní syntaxe příkazu je následující:

```
id [možnosti] [argumenty]
```

## Běžné možnosti
- `-u`: Zobrazí pouze uživatelské ID (UID).
- `-g`: Zobrazí pouze primární skupinové ID (GID).
- `-G`: Zobrazí všechna skupinová ID, do kterých uživatel patří.
- `-n`: Zobrazí jména místo číselných ID.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `id`:

1. Zobrazení informací o aktuálním uživateli:
   ```sh
   id
   ```

2. Zobrazení pouze uživatelského ID aktuálního uživatele:
   ```sh
   id -u
   ```

3. Zobrazení pouze primárního skupinového ID aktuálního uživatele:
   ```sh
   id -g
   ```

4. Zobrazení všech skupinových ID aktuálního uživatele:
   ```sh
   id -G
   ```

5. Zobrazení informací o jiném uživateli (např. uživatel "jan"):
   ```sh
   id jan
   ```

## Tipy
- Používejte volbu `-n`, pokud chcete vidět jména skupin místo číselných ID, což může být užitečné pro lepší orientaci.
- Příkaz `id` je rychlý a efektivní způsob, jak zjistit oprávnění uživatelů, zejména při správě systému.
- Pokud potřebujete zkontrolovat oprávnění skriptu nebo programu, můžete použít `id` k ověření, zda má správný uživatel potřebná oprávnění.