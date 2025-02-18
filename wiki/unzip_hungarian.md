# [Debian] Debian Almquist Shell (dash) unzip használata: Fájlok kicsomagolása ZIP archívumból

## Áttekintés
Az `unzip` parancs a ZIP archívumok kicsomagolására szolgál. Lehetővé teszi a felhasználók számára, hogy a tömörített fájlokat visszaállítsák az eredeti formájukba.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
unzip [opciók] [argumentumok]
```

## Gyakori opciók
- `-l`: Listázza a ZIP fájl tartalmát anélkül, hogy kicsomagolná.
- `-d`: Megadja a célmappát, ahová a fájlokat kicsomagolják.
- `-o`: Felülírja a meglévő fájlokat anélkül, hogy megerősítést kérne.
- `-q`: Csendes mód, amely csökkenti a kimenetet.

## Gyakori példák
1. ZIP fájl kicsomagolása az aktuális könyvtárba:
   ```bash
   unzip fajl.zip
   ```

2. ZIP fájl tartalmának listázása:
   ```bash
   unzip -l fajl.zip
   ```

3. ZIP fájl kicsomagolása egy megadott mappába:
   ```bash
   unzip fajl.zip -d /path/to/directory
   ```

4. ZIP fájl kicsomagolása, meglévő fájlok felülírásával:
   ```bash
   unzip -o fajl.zip
   ```

5. Csendes kicsomagolás, kevesebb kimenettel:
   ```bash
   unzip -q fajl.zip
   ```

## Tippek
- Mindig ellenőrizd a ZIP fájl tartalmát a `-l` opcióval, mielőtt kicsomagolnád, hogy elkerüld a nem kívánt fájlok kicsomagolását.
- Használj külön mappát a kicsomagolt fájlok számára, hogy rendszerezettebb maradj.
- Ha gyakran dolgozol jelszóval védett ZIP fájlokkal, érdemes megismerkedni a `-P` opcióval, amely lehetővé teszi a jelszó megadását a kicsomagolás során.