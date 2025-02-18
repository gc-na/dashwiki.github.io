# [Debian] Debian Almquist Shell (dash) bzip2 használata: Fájlok tömörítése és kitömörítése

## Áttekintés
A `bzip2` parancs egy tömörítő eszköz, amely a fájlok méretének csökkentésére szolgál. A bzip2 algoritmus hatékonyan tömöríti a fájlokat, így azok kevesebb helyet foglalnak el a lemezen, és gyorsabban átkonvertálhatók vagy továbbíthatók.

## Használat
A `bzip2` parancs alapvető szintaxisa a következő:

```bash
bzip2 [opciók] [argumentumok]
```

## Gyakori opciók
- `-d`, `--decompress`: A tömörített fájlok kitömörítésére szolgál.
- `-k`, `--keep`: Megőrzi az eredeti fájlt a tömörítés során.
- `-f`, `--force`: Kényszeríti a tömörítést, még akkor is, ha a célfájl már létezik.
- `-v`, `--verbose`: Részletes kimenetet ad a tömörítési folyamatról.

## Gyakori példák
1. Fájl tömörítése:
   ```bash
   bzip2 fájl.txt
   ```
   Ez a parancs létrehozza a `fájl.txt.bz2` tömörített fájlt, és törli az eredeti `fájl.txt` fájlt.

2. Fájl kitömörítése:
   ```bash
   bzip2 -d fájl.txt.bz2
   ```
   Ez a parancs visszaállítja az eredeti `fájl.txt` fájlt a tömörített `fájl.txt.bz2` fájlból.

3. Eredeti fájl megőrzése tömörítéskor:
   ```bash
   bzip2 -k fájl.txt
   ```
   A parancs létrehozza a `fájl.txt.bz2` fájlt, de az eredeti `fájl.txt` fájl megmarad.

4. Tömörített fájl kényszerített felülírása:
   ```bash
   bzip2 -f fájl.txt
   ```
   Ha a `fájl.txt.bz2` már létezik, a parancs felülírja azt.

## Tippek
- Mindig ellenőrizd a fájl méretét a tömörítés előtt és után, hogy lásd a megtakarítást.
- Használj `-v` opciót, ha szeretnéd nyomon követni a tömörítési folyamatot.
- A `bzip2` parancs ideális nagy méretű szöveges fájlok tömörítésére, mivel a tömörítési arány általában jobb, mint más algoritmusoké.