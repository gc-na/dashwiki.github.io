# [Debian] Debian Almquist Shell (dash) comm parancs: Két fájl összehasonlítása

## Overview
A `comm` parancs két fájl sorait hasonlítja össze, és három oszlopban jeleníti meg az eltéréseket: az első oszlop a csak az első fájlban található sorokat, a második oszlop a csak a második fájlban található sorokat, a harmadik oszlop pedig a közös sorokat tartalmazza.

## Usage
A `comm` parancs alapvető szintaxisa a következő:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Az első oszlop (csak az első fájlban található sorok) elrejtése.
- `-2`: A második oszlop (csak a második fájlban található sorok) elrejtése.
- `-3`: A harmadik oszlop (közös sorok) elrejtése.
- `-i`: A kis- és nagybetűk figyelmen kívül hagyása a hasonlítás során.

## Common Examples
1. **Alapértelmezett használat**: Két fájl összehasonlítása és az eltérések megjelenítése.
   ```bash
   comm file1.txt file2.txt
   ```

2. **Csak az első fájlban található sorok megjelenítése**:
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. **Csak a második fájlban található sorok megjelenítése**:
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. **Közös sorok megjelenítése**:
   ```bash
   comm -23 file1.txt file2.txt
   ```

5. **Kis- és nagybetűk figyelmen kívül hagyása**:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- Győződj meg róla, hogy a fájlok rendezettek, mivel a `comm` csak rendezett fájlokkal működik helyesen.
- Használj csővezetékeket (`|`) más parancsokkal, hogy a `comm` kimenetét további feldolgozásra használd.
- A `sort` parancsot használhatod a fájlok rendezésére, mielőtt a `comm`-ot alkalmaznád:
  ```bash
  sort file1.txt > sorted_file1.txt
  sort file2.txt > sorted_file2.txt
  comm sorted_file1.txt sorted_file2.txt
  ```