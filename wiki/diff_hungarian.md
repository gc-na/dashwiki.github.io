# [Debian] Debian Almquist Shell (dash) diff használata: fájlok közötti eltérések megjelenítése

## Áttekintés
A `diff` parancs a fájlok közötti eltérések megjelenítésére szolgál. Összehasonlítja a megadott fájlokat, és kiemeli azokat a sorokat, amelyek eltérnek egymástól.

## Használat
A `diff` parancs alapvető szintaxisa a következő:

```bash
diff [opciók] [argumentumok]
```

## Gyakori opciók
- `-u`: Egységes formátumú kimenetet ad, amely könnyebben olvasható.
- `-i`: Figyelmen kívül hagyja a kis- és nagybetűk közötti eltéréseket.
- `-w`: Figyelmen kívül hagyja a szóközöket és a tabulátorokat.
- `-r`: Rekurzívan hasonlítja össze a könyvtárakat.

## Gyakori példák
1. Két fájl összehasonlítása:
   ```bash
   diff file1.txt file2.txt
   ```

2. Egységes formátumú kimenet megjelenítése:
   ```bash
   diff -u file1.txt file2.txt
   ```

3. Kis- és nagybetűk figyelmen kívül hagyása:
   ```bash
   diff -i file1.txt file2.txt
   ```

4. Két könyvtár rekurzív összehasonlítása:
   ```bash
   diff -r dir1/ dir2/
   ```

## Tippek
- Használj `-u` opciót, ha a kimenetet könnyebben olvasható formátumban szeretnéd látni.
- A `diff` kimenetei alapján a `patch` parancs segítségével könnyen alkalmazhatsz módosításokat.
- Ellenőrizd a fájlok kódolását, mivel a különböző kódolások eltérő eredményeket adhatnak.