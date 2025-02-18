# [Debian] Debian Almquist Shell (dash) unxz használat: Fájlok kicsomagolása

## Áttekintés
Az `unxz` parancs a `.xz` tömörített fájlok kicsomagolására szolgál. Ez a parancs a XZ formátumú fájlokat visszaállítja az eredeti, tömörítetlen állapotukba.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
unxz [opciók] [argumentumok]
```

## Gyakori opciók
- `-k`, `--keep`: Megőrzi az eredeti `.xz` fájlt a kicsomagolás után.
- `-f`, `--force`: Kényszeríti a kicsomagolást, még akkor is, ha a célfájl már létezik.
- `-v`, `--verbose`: Részletes információt ad a kicsomagolás folyamatáról.

## Gyakori példák
1. Egy `.xz` fájl kicsomagolása:
   ```bash
   unxz fájl.xz
   ```

2. Az eredeti fájl megőrzése a kicsomagolás után:
   ```bash
   unxz -k fájl.xz
   ```

3. Kényszerített kicsomagolás, ha a célfájl már létezik:
   ```bash
   unxz -f fájl.xz
   ```

4. Részletes kicsomagolási folyamat megjelenítése:
   ```bash
   unxz -v fájl.xz
   ```

## Tippek
- Mindig ellenőrizd, hogy van-e elegendő hely a célmappában a kicsomagolt fájl számára.
- Használj `-k` opciót, ha nem szeretnéd elveszíteni az eredeti tömörített fájlt.
- A `-v` opció hasznos lehet, ha szeretnéd nyomon követni a kicsomagolás folyamatát, különösen nagy fájlok esetén.