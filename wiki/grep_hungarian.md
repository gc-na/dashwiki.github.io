# [Debian] Debian Almquist Shell (dash) grep használata: Szöveg keresése fájlokban

## Overview
A `grep` parancs egy rendkívül hasznos eszköz a szöveges fájlokban történő kereséshez. Lehetővé teszi, hogy meghatározott mintákat keressünk a fájlokban, és azokat a sorokat jelenítjük meg, amelyek megfelelnek a keresett kifejezésnek.

## Usage
A `grep` parancs alapvető szintaxisa a következő:

```bash
grep [opciók] [argumentumok]
```

## Common Options
- `-i`: Figyelmen kívül hagyja a kis- és nagybetűk közötti különbséget.
- `-v`: Csak azokat a sorokat jeleníti meg, amelyek nem tartalmazzák a keresett mintát.
- `-r`: Rekurzívan keres a megadott könyvtárban.
- `-n`: Megjeleníti a sorok számát, ahol a minta megtalálható.
- `-l`: Csak a fájlok nevét listázza, amelyek tartalmazzák a keresett mintát.

## Common Examples
1. Alapvető keresés egy fájlban:
   ```bash
   grep "minta" fajl.txt
   ```

2. Kis- és nagybetűk figyelmen kívül hagyása:
   ```bash
   grep -i "minta" fajl.txt
   ```

3. Keresés rekurzívan egy könyvtárban:
   ```bash
   grep -r "minta" /elérési/út/
   ```

4. Sorok számának megjelenítése:
   ```bash
   grep -n "minta" fajl.txt
   ```

5. Csak a fájlok neveinek listázása:
   ```bash
   grep -l "minta" *.txt
   ```

## Tips
- Használj reguláris kifejezéseket a keresési minták pontosabb meghatározásához.
- Kombináld a `grep` parancsot más parancsokkal, például a `pipe` (`|`) operátorral, hogy a kimenetet további feldolgozásra használd.
- Ha nagy fájlokkal dolgozol, érdemes a `-m` opciót használni, hogy korlátozd a találatok számát, ezzel gyorsabbá téve a keresést.