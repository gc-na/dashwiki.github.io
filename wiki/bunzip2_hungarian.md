# [Debian] Debian Almquist Shell (dash) bunzip2 használata: Fájlok kicsomagolása

## Áttekintés
A `bunzip2` parancs a bzip2 tömörített fájlok kicsomagolására szolgál. Ez a parancs visszaállítja az eredeti fájlt a tömörített formátumból, lehetővé téve a felhasználók számára, hogy hozzáférjenek az adatokhoz.

## Használat
A `bunzip2` parancs alapvető szintaxisa a következő:

```bash
bunzip2 [opciók] [argumentumok]
```

## Gyakori opciók
- `-k`: Megőrzi az eredeti, tömörített fájlt a kicsomagolás után is.
- `-f`: Kényszeríti a kicsomagolást, még akkor is, ha a kicsomagolt fájl már létezik.
- `-v`: Részletes kimenetet ad a kicsomagolás folyamatáról.

## Gyakori példák
1. **Egyszerű kicsomagolás**
   ```bash
   bunzip2 fájl.bz2
   ```

2. **Eredeti fájl megőrzése**
   ```bash
   bunzip2 -k fájl.bz2
   ```

3. **Kényszerített kicsomagolás**
   ```bash
   bunzip2 -f fájl.bz2
   ```

4. **Részletes kimenet**
   ```bash
   bunzip2 -v fájl.bz2
   ```

## Tippek
- Mindig ellenőrizd, hogy van-e elegendő hely a lemezen a kicsomagolt fájl számára.
- Használj `-k` opciót, ha nem szeretnéd elveszíteni a tömörített fájlt.
- A `bunzip2` parancsot gyakran használják scriptelés során, így érdemes automatizálni a folyamatokat, ha rendszeresen kicsomagolsz fájlokat.