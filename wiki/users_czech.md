# [Český] Debian Almquist Shell (dash) uživatelé příkaz: Zobrazí seznam uživatelů

## Přehled
Příkaz `users` v shellu dash slouží k zobrazení seznamu uživatelů, kteří jsou aktuálně přihlášeni do systému. Tento příkaz je užitečný pro rychlé zjištění, kdo je na systému aktivní.

## Použití
Základní syntaxe příkazu je následující:

```bash
users [options] [arguments]
```

## Běžné možnosti
Příkaz `users` nemá mnoho možností, ale zde jsou některé z nich:

- `-n` : Zobrazí pouze unikátní uživatelská jména.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `users`:

1. Zobrazit seznam všech aktuálně přihlášených uživatelů:

   ```bash
   users
   ```

2. Zobrazit unikátní uživatelská jména:

   ```bash
   users -n
   ```

## Tipy
- Příkaz `users` je užitečné kombinovat s dalšími příkazy, jako je `who` nebo `w`, pro získání podrobnějších informací o uživatelích.
- Mějte na paměti, že příkaz `users` zobrazuje pouze uživatele, kteří jsou aktuálně přihlášeni, a ne všechny uživatelské účty v systému.