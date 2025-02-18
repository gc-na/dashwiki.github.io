# [Debian] Debian Almquist Shell (dash) free: memóriahasználat megjelenítése

## Áttekintés
A `free` parancs a rendszer memóriahasználatának megjelenítésére szolgál. Információt nyújt a használt, szabad és a swap memóriáról, ami segít a rendszer teljesítményének nyomon követésében.

## Használat
A `free` parancs alapvető szintaxisa a következő:

```bash
free [opciók] [argumentumok]
```

## Gyakori opciók
- `-h`: Ember által olvasható formátumban jeleníti meg az adatokat (pl. MB, GB).
- `-m`: Az adatokat megabájtban jeleníti meg.
- `-g`: Az adatokat gigabájtban jeleníti meg.
- `-s <másodperc>`: Folyamatosan frissíti az információkat a megadott másodperces intervallumban.
- `-t`: Összesíti a memóriahasználatot, beleértve a swap memóriát is.

## Gyakori példák
1. Alap memóriahasználat megjelenítése:
   ```bash
   free
   ```

2. Ember által olvasható formátumban:
   ```bash
   free -h
   ```

3. Memóriahasználat megjelenítése megabájtban:
   ```bash
   free -m
   ```

4. Folyamatos frissítés 5 másodpercenként:
   ```bash
   free -s 5
   ```

5. Összesített memóriahasználat megjelenítése:
   ```bash
   free -t
   ```

## Tippek
- Használja a `-h` opciót, hogy könnyebben értelmezhető formátumban láthassa a memóriahasználatot.
- A `free` parancsot kombinálhatja más parancsokkal, például a `watch`-al, hogy folyamatosan figyelje a memóriahasználatot:
  ```bash
  watch free -h
  ```
- Rendszeres ellenőrzés a memóriahasználatról segíthet az esetleges problémák korai észlelésében.