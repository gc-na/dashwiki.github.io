# [Debian] Debian Almquist Shell (dash) gunzip használata: Fájlok kicsomagolása

## Áttekintés
A `gunzip` parancs a Gzip tömörített fájlok kicsomagolására szolgál. Ez a parancs lehetővé teszi a felhasználók számára, hogy visszaállítsák az eredeti fájlokat a Gzip formátumból.

## Használat
A `gunzip` parancs alapvető szintaxisa a következő:

```bash
gunzip [opciók] [argumentumok]
```

## Gyakori opciók
- `-c`: A kicsomagolt fájlt a standard kimenetre írja, ahelyett, hogy fájlba mentené.
- `-f`: Kényszeríti a fájlok felülírását, ha már léteznek.
- `-k`: Megőrzi az eredeti tömörített fájlt a kicsomagolás után is.
- `-v`: Részletes kimenetet ad, amely megmutatja a kicsomagolt fájlokat.

## Gyakori példák
1. **Alap kicsomagolás**:
   ```bash
   gunzip fájl.gz
   ```

2. **Kicsomagolás a standard kimenetre**:
   ```bash
   gunzip -c fájl.gz > új_fájl
   ```

3. **Fájlok felülírása**:
   ```bash
   gunzip -f fájl.gz
   ```

4. **Eredeti fájl megőrzése**:
   ```bash
   gunzip -k fájl.gz
   ```

5. **Részletes kimenet**:
   ```bash
   gunzip -v fájl.gz
   ```

## Tippek
- Mindig ellenőrizd, hogy van-e elegendő hely a lemezen a kicsomagolt fájlok számára.
- Használj `-k` opciót, ha nem szeretnéd elveszíteni az eredeti tömörített fájlt.
- A `-c` opció hasznos lehet, ha a kicsomagolt adatokat közvetlenül egy másik parancsnak szeretnéd átadni.