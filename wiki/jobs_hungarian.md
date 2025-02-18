# [Debian] Debian Almquist Shell (dash) jobs használata: háttérfolyamatok kezelése

## Overview
A `jobs` parancs a háttérben futó folyamatok listázására szolgál a shell környezetben. Segítségével nyomon követhetjük a háttérben futó feladatokat, és információt kaphatunk azok állapotáról.

## Usage
A parancs alapvető szintaxisa a következő:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Megjeleníti a folyamatok PID-jét (Process ID).
- `-n`: Csak azokat a folyamatokat listázza, amelyek állapota megváltozott az utolsó futtatás óta.
- `-p`: Csak a folyamatok PID-jét jeleníti meg.

## Common Examples
1. **Folyamatok listázása**:
   A háttérben futó folyamatok egyszerű listázása:
   ```bash
   jobs
   ```

2. **PID-ek megjelenítése**:
   A folyamatok PID-jének megjelenítése:
   ```bash
   jobs -l
   ```

3. **Állapotváltozások figyelése**:
   Csak az állapotváltozással rendelkező folyamatok listázása:
   ```bash
   jobs -n
   ```

4. **Csak PID-ek listázása**:
   Csak a háttérben futó folyamatok PID-jeinek megjelenítése:
   ```bash
   jobs -p
   ```

## Tips
- Használja a `jobs` parancsot a háttérben futó folyamatok nyomon követésére, mielőtt kilépne a shellből, hogy elkerülje a folyamatok elvesztését.
- A `fg` és `bg` parancsokkal együtt használva könnyen átviheti a folyamatokat a háttérből az előtérbe, vagy fordítva.
- Figyeljen a folyamatok állapotára, mivel a `jobs` parancs nem mutatja az összes futó folyamatot, csak azokat, amelyeket a jelenlegi shell indított.