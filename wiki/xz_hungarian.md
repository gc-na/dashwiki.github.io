# [Debian] Debian Almquist Shell (dash) xz használata: Fájlok tömörítése és kicsomagolása

## Áttekintés
Az `xz` parancs egy tömörítő eszköz, amely a fájlok méretének csökkentésére szolgál. Az `xz` formátum általában jobb tömörítési arányt kínál, mint más hagyományos tömörítési módszerek, mint például a gzip.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
xz [opciók] [argumentumok]
```

## Gyakori opciók
- `-d`, `--decompress`: A fájl kicsomagolása.
- `-k`, `--keep`: Az eredeti fájl megtartása a tömörítés után.
- `-f`, `--force`: A fájlok felülírása, ha már léteznek.
- `-z`, `--compress`: A fájlok tömörítése (ez az alapértelmezett művelet).
- `-9`: Maximális tömörítési szint.

## Gyakori példák
1. Fájl tömörítése:
   ```bash
   xz fájl.txt
   ```

2. Fájl kicsomagolása:
   ```bash
   xz -d fájl.txt.xz
   ```

3. Eredeti fájl megtartása tömörítéskor:
   ```bash
   xz -k fájl.txt
   ```

4. Maximális tömörítési szint alkalmazása:
   ```bash
   xz -9 fájl.txt
   ```

5. Több fájl tömörítése egyszerre:
   ```bash
   xz fájl1.txt fájl2.txt fájl3.txt
   ```

## Tippek
- Használj `-k` opciót, ha szeretnéd megtartani az eredeti fájlokat a tömörítés után.
- A maximális tömörítési szint (`-9`) használata több időt vehet igénybe, ezért érdemes mérlegelni, hogy szükséges-e.
- Az `xz` fájlok kicsomagolásához a `-d` opció mellett használhatod a `unxz` parancsot is, amely egy szinonimája az `xz -d` parancsnak.