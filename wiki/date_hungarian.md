# [Debian] Debian Almquist Shell (dash) date: dátum és idő megjelenítése

## Overview
A `date` parancs a rendszer aktuális dátumát és időpontját jeleníti meg. Lehetővé teszi a felhasználók számára, hogy különböző formátumokban kérjék le az időt és a dátumot, valamint beállíthatják a rendszerdátumot és időt is.

## Usage
A parancs alapvető szintaxisa a következő:

```bash
date [options] [arguments]
```

## Common Options
- `-u`: Az UTC (Coordinated Universal Time) időzónát használja.
- `+FORMAT`: A megjelenítési formátum megadása, ahol a FORMAT a kívánt formátumot jelöli.
- `-d STRING`: Egy adott dátumot és időt ad meg, amelyet a STRING formátumban kell megadni.

## Common Examples
- Az aktuális dátum és idő megjelenítése:
    ```bash
    date
    ```

- Az aktuális dátum és idő UTC időzónában:
    ```bash
    date -u
    ```

- Dátum megjelenítése egyedi formátumban (pl. Év-Hónap-Nap):
    ```bash
    date "+%Y-%m-%d"
    ```

- Egy adott dátum megjelenítése (pl. 2023. október 1.):
    ```bash
    date -d "2023-10-01"
    ```

## Tips
- Használj formátumokat a `+FORMAT` opcióval, hogy a dátumot és időt a saját igényeid szerint jelenítsd meg.
- Ellenőrizd a rendszer időzónáját a `date` parancs futtatásával, hogy biztos legyél benne, hogy a megfelelő időt látod.
- A `date` parancs segítségével könnyen beállíthatod a rendszer időpontját, de légy óvatos, mert ez adminisztrátori jogosultságokat igényel.