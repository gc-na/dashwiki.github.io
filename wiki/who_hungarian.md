# [Debian] Debian Almquist Shell (dash) who: Felhasználók listázása

## Overview
A `who` parancs megjeleníti a jelenleg bejelentkezett felhasználók listáját a rendszerre. Hasznos információkat nyújt a felhasználókról, például a bejelentkezésük időpontját és a használt terminálokat.

## Usage
A `who` parancs alapvető szintaxisa a következő:

```bash
who [opciók] [argumentumok]
```

## Common Options
- `-a`: Minden elérhető információt megjelenít a felhasználókról.
- `-b`: Megjeleníti a legutóbbi rendszerindítás időpontját.
- `-q`: Csak a felhasználók számát és nevét mutatja.
- `--help`: Megjeleníti a parancs használati útmutatóját.

## Common Examples
1. **Alapvető használat**: A jelenlegi bejelentkezett felhasználók listázása.
   ```bash
   who
   ```

2. **Minden információ megjelenítése**: Részletes információk a felhasználókról.
   ```bash
   who -a
   ```

3. **Rendszerindítás időpontjának megjelenítése**:
   ```bash
   who -b
   ```

4. **Csak a felhasználók számának és nevüknek megjelenítése**:
   ```bash
   who -q
   ```

## Tips
- Használja a `who` parancsot rendszeres időközönként, hogy nyomon követhesse, kik vannak bejelentkezve a rendszerre.
- A `who` parancs kimenete hasznos lehet a rendszeradminisztrátorok számára a felhasználói aktivitás figyelemmel kísérésére.
- Kombinálja a `who` parancsot más parancsokkal, például a `grep`-pel, hogy szűkítse a keresést egy adott felhasználóra.