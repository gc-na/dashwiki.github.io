# [Debian] Debian Almquist Shell (dash) cal használata: naptár megjelenítése

## Áttekintés
A `cal` parancs egy egyszerű eszköz, amely lehetővé teszi a felhasználók számára, hogy naptárakat jelenítsenek meg a terminálban. Ezzel a parancssal könnyen megtekinthetjük a hónapok és évek naptárait, ami hasznos lehet időpontok és események nyomon követésére.

## Használat
A `cal` parancs alapvető szintaxisa a következő:

```bash
cal [opciók] [argumentumok]
```

## Gyakori Opciók
- `-m`: A hónap első napját hétfőként jeleníti meg.
- `-y`: Az aktuális év naptárát jeleníti meg.
- `-3`: A megadott hónap előtt és után egy-egy hónapot is megjelenít.
- `-j`: A naptárat Julianus napokkal együtt mutatja.
- `-A [n]`: A megadott hónap után `n` hónapot is megjelenít.
- `-B [n]`: A megadott hónap előtt `n` hónapot is megjelenít.

## Gyakori Példák
1. Az aktuális hónap naptárának megjelenítése:
   ```bash
   cal
   ```

2. Egy adott hónap (2023. december) naptárának megjelenítése:
   ```bash
   cal 12 2023
   ```

3. Az aktuális év naptárának megjelenítése:
   ```bash
   cal -y
   ```

4. A 2023. július hónap naptárának megjelenítése a június és augusztus hónapokkal együtt:
   ```bash
   cal -3 7 2023
   ```

5. A naptár Julianus napokkal való megjelenítése:
   ```bash
   cal -j
   ```

## Tippek
- Használj `cal -m` opciót, ha szeretnéd, hogy a hétfő legyen a hét első napja, ami sok országban a megszokott.
- A `cal` parancsot kombinálhatod más parancsokkal is, például a `grep`-pel, hogy keresd a fontos dátumokat.
- Érdemes megismerkedni a `man cal` parancs használatával, hogy részletesebb információkat kapj a parancs lehetőségeiről.