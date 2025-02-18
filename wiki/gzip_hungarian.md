# [Debian] Debian Almquist Shell (dash) gzip használata: Fájlok tömörítése

## Áttekintés
A `gzip` parancs a GNU tömörítő program, amelyet fájlok tömörítésére használnak, hogy csökkentsék azok méretét. A tömörített fájlok általában `.gz` kiterjesztéssel rendelkeznek, és a `gzip` a leggyakrabban használt tömörítési módszer a Unix-alapú rendszerekben.

## Használat
A `gzip` parancs alapvető szintaxisa a következő:

```bash
gzip [opciók] [argumentumok]
```

## Gyakori opciók
- `-d`, `--decompress`: A tömörített fájlok kicsomagolására szolgál.
- `-k`, `--keep`: Megőrzi az eredeti fájlt a tömörítés során.
- `-v`, `--verbose`: Részletes információt ad a tömörítési folyamatról.
- `-r`, `--recursive`: Rekurzívan tömöríti a könyvtárakat.

## Gyakori példák
Több gyakorlati példa a `gzip` használatára:

1. Fájl tömörítése:
   ```bash
   gzip file.txt
   ```

2. Fájl kicsomagolása:
   ```bash
   gzip -d file.txt.gz
   ```

3. Eredeti fájl megőrzése tömörítéskor:
   ```bash
   gzip -k file.txt
   ```

4. Több fájl tömörítése egyszerre:
   ```bash
   gzip file1.txt file2.txt
   ```

5. Rekurzív tömörítés egy könyvtárban:
   ```bash
   gzip -r my_directory/
   ```

## Tippek
- Mindig ellenőrizd a fájlok méretét a tömörítés előtt és után, hogy lásd a megtakarítást.
- Használj `-v` opciót, ha szeretnéd látni a tömörítési folyamat részleteit.
- Ha gyakran dolgozol tömörített fájlokkal, érdemes lehet megismerkedni a `gunzip` parancs használatával is a kicsomagoláshoz.