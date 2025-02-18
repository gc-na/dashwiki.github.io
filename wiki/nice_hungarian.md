# [Debian] Debian Almquist Shell (dash) nice használata: A folyamatok prioritásának beállítása

## Áttekintés
A `nice` parancs a Debian Almquist Shell (dash) környezetében lehetővé teszi a felhasználók számára, hogy beállítsák a folyamatok prioritását. Ezzel a paranccsal csökkenthetjük vagy növelhetjük egy adott folyamat CPU-hoz való hozzáférésének mértékét, így segítve a rendszer teljesítményének optimalizálását.

## Használat
A `nice` parancs alapvető szintaxisa a következő:

```bash
nice [opciók] [parancs] [argumentumok]
```

## Gyakori opciók
- `-n, --adjustment`: A prioritás módosítása, ahol a megadott szám növelheti (pozitív szám) vagy csökkentheti (negatív szám) a prioritást.
- `-h, --help`: Információ a parancsról és a használatáról.
- `-v, --version`: A `nice` parancs verziójának megjelenítése.

## Gyakori példák
1. Alapértelmezett prioritás beállítása egy parancs futtatásához:
   ```bash
   nice sleep 10
   ```

2. Egy parancs prioritásának csökkentése (növelve a nice értéket):
   ```bash
   nice -n 10 myscript.sh
   ```

3. Egy parancs prioritásának növelése (csökkentve a nice értéket):
   ```bash
   nice -n -5 myscript.sh
   ```

4. A `nice` parancs használata háttérben futó folyamatokhoz:
   ```bash
   nice -n 15 long_running_process &
   ```

## Tippek
- Használj alacsonyabb nice értéket (pl. -5) a fontosabb folyamatok számára, hogy azok előnyben részesüljenek a CPU használat során.
- Legyél óvatos a magas nice értékek (pl. 19) használatával, mivel ezek jelentősen lelassíthatják a folyamatokat.
- Ellenőrizd a folyamatok prioritását a `ps` vagy `top` parancsokkal, hogy lásd, hogyan befolyásolják a rendszer teljesítményét.