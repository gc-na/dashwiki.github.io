# [Debian] Debian Almquist Shell (dash) du használata: Fájlok és könyvtárak méretének megjelenítése

## Áttekintés
A `du` (disk usage) parancs a fájlok és könyvtárak lemezhasználatának megjelenítésére szolgál. Segítségével könnyen ellenőrizhetjük, hogy mennyi helyet foglalnak el a különböző fájlok és mappák a fájlrendszerben.

## Használat
A `du` parancs alapvető szintaxisa a következő:

```bash
du [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Emberi olvasható formátumban jeleníti meg a méreteket (pl. KB, MB).
- `-s`: Csak a megadott könyvtár összesített méretét mutatja.
- `-a`: Minden fájl és könyvtár méretét megjeleníti, nem csak a könyvtárakat.
- `-c`: Összesíti a megadott könyvtárak méretét és megjeleníti az összesített értéket.

## Gyakori példák
1. A jelenlegi könyvtár méretének megjelenítése:
   ```bash
   du -h
   ```

2. Egy adott könyvtár összesített méretének megjelenítése:
   ```bash
   du -sh /path/to/directory
   ```

3. Minden fájl és könyvtár méretének megjelenítése a jelenlegi könyvtárban:
   ```bash
   du -ah
   ```

4. Több könyvtár összesített méretének megjelenítése:
   ```bash
   du -ch /path/to/directory1 /path/to/directory2
   ```

## Tippek
- Használja a `-h` opciót, hogy a méreteket könnyebben értelmezhető formátumban láthassa.
- A `-s` opcióval gyorsan megtudhatja, hogy egy könyvtár mennyi helyet foglal el anélkül, hogy a részletekbe menne.
- Ha sok fájl van egy könyvtárban, érdemes a `-a` opciót használni a részletesebb információkért.