# [Debian] Debian Almquist Shell (dash) users parancs: Felhasználók listázása

## Áttekintés
A `users` parancs a jelenleg bejelentkezett felhasználók nevét listázza ki a rendszerben. Ez a parancs hasznos lehet a rendszeradminisztrátorok számára, hogy gyorsan áttekintsék, kik vannak bejelentkezve.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
users [opciók]
```

## Gyakori opciók
A `users` parancsnak nincsenek különösebb opciói, mivel a fő célja a bejelentkezett felhasználók nevének egyszerű megjelenítése. Azonban a következő opciók használhatók:

- `-n`: A felhasználók nevét nem jeleníti meg, csak a számukat adja vissza.

## Gyakori példák
Itt van néhány példa a `users` parancs használatára:

1. **Jelenlegi felhasználók listázása:**
   ```bash
   users
   ```

2. **Felhasználók számának megjelenítése:**
   ```bash
   users -n
   ```

## Tippek
- Használja a `who` parancsot a bejelentkezett felhasználók részletesebb információinak megtekintéséhez, például a bejelentkezés idejét és a terminál nevét.
- A `users` parancs kimenete egyszerű, ezért könnyen beilleszthető más parancsokba, például a `wc` (word count) parancsba a felhasználók számának megszámlálásához:
  ```bash
  users | wc -w
  ```