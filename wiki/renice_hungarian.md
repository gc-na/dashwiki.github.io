# [Debian] Debian Almquist Shell (dash) renice: A folyamat prioritásának módosítása

## Áttekintés
A `renice` parancs lehetővé teszi a már futó folyamatok prioritásának módosítását a Linux operációs rendszerekben. A prioritás megváltoztatásával befolyásolhatjuk, hogy a rendszer mennyire részesíti előnyben a folyamatot a CPU erőforrások elosztásakor.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
renice [opciók] [argumentumok]
```

## Gyakori opciók
- `-n, --priority`: A prioritás értéke, amelyet be szeretnénk állítani. Az értékek -20 (legmagasabb prioritás) és 19 (legalacsonyabb prioritás) között mozognak.
- `-p, --pid`: A módosítani kívánt folyamat azonosítója (PID).
- `-g, --pgrp`: A módosítani kívánt folyamatcsoport azonosítója.
- `-u, --user`: A módosítani kívánt felhasználó összes folyamatának prioritása.

## Gyakori példák
1. Folyamat prioritásának növelése (pl. PID 1234 esetén):
   ```bash
   renice -n -5 -p 1234
   ```

2. Folyamat prioritásának csökkentése (pl. PID 5678 esetén):
   ```bash
   renice -n 10 -p 5678
   ```

3. Az összes folyamat prioritásának módosítása egy adott felhasználó számára (pl. "username"):
   ```bash
   renice -n 5 -u username
   ```

4. Folyamatcsoport prioritásának módosítása (pl. csoport azonosító 1000):
   ```bash
   renice -n 0 -g 1000
   ```

## Tippek
- Mindig ellenőrizd a folyamatok prioritását a `ps` vagy `top` parancsokkal, mielőtt módosítanád őket.
- A `renice` parancs használatához rendszergazdai jogosultságokra lehet szükség, különösen, ha a prioritás csökkentését szeretnéd végrehajtani.
- Használj alacsonyabb prioritású értékeket a nem kritikus folyamatokhoz, hogy a fontosabb feladatok számára több CPU időt biztosíts.