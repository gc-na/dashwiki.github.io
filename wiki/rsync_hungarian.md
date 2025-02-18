# [Debian] Debian Almquist Shell (dash) rsync használata: Fájlok szinkronizálása

## Áttekintés
Az `rsync` parancs egy hatékony eszköz, amely lehetővé teszi fájlok és könyvtárak szinkronizálását helyi és távoli rendszerek között. Az `rsync` különösen hasznos, mert csak a változásokat másolja át, így csökkenti az átvitel idejét és a sávszélesség használatát.

## Használat
Az `rsync` parancs alapvető szintaxisa a következő:

```bash
rsync [opciók] [forrás] [cél]
```

## Gyakori Opciók
- `-a`: Archiválás mód, amely megőrzi a fájlok tulajdonságait (pl. jogosultságok, időbélyegek).
- `-v`: Verbose (részletes) mód, amely megjeleníti a másolás folyamatát.
- `-z`: Tömöríti az adatokat az átvitel során, csökkentve a sávszélesség használatát.
- `-r`: Rekurzív másolás, amely lehetővé teszi könyvtárak másolását.
- `--delete`: Törli a célmappából azokat a fájlokat, amelyek a forrásmappában már nem találhatók.

## Gyakori Példák
1. Fájlok másolása helyi könyvtárak között:
   ```bash
   rsync -av /forras/konyvtar/ /cel/konyvtar/
   ```

2. Fájlok másolása távoli szerverre SSH-n keresztül:
   ```bash
   rsync -avz /helyi/fajl.txt felhasznalo@tavoli-szerver:/tavoli/konyvtar/
   ```

3. Könyvtár szinkronizálása, törölve a felesleges fájlokat a célból:
   ```bash
   rsync -av --delete /forras/konyvtar/ /cel/konyvtar/
   ```

4. Fájlok másolása tömörítéssel:
   ```bash
   rsync -avz /forras/konyvtar/ felhasznalo@tavoli-szerver:/tavoli/konyvtar/
   ```

## Tippek
- Mindig használj `-n` (dry run) opciót, hogy először ellenőrizd, mit fog tenni a parancs, mielőtt ténylegesen végrehajtanád.
- Használj `--progress` opciót, hogy nyomon követhesd a másolás előrehaladását.
- Ha nagy mennyiségű fájlt másolsz, érdemes lehet a `--bwlimit` opciót használni a sávszélesség korlátozására, hogy ne terheld le a hálózatot.