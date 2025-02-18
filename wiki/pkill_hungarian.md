# [Debian] Debian Almquist Shell (dash) pkill használata: Folyamatok leállítása név alapján

## Áttekintés
A `pkill` parancs lehetővé teszi a folyamatok leállítását a nevük alapján. Ez egy kényelmes eszköz, amely segít a rendszergazdáknak és a felhasználóknak a nem kívánt folyamatok gyors eltávolításában.

## Használat
A `pkill` parancs alapvető szintaxisa a következő:

```bash
pkill [opciók] [argumentumok]
```

## Gyakori opciók
- `-f`: A parancssor teljes szövegét figyelembe veszi a folyamatok azonosításakor.
- `-n`: Csak a legutoljára indított folyamatot állítja le.
- `-o`: Csak a legrégebben indított folyamatot állítja le.
- `-signal`: Megadja a leállításhoz használandó jelet (alapértelmezett: TERM).

## Gyakori példák
1. **Folyamat leállítása név alapján**:
   ```bash
   pkill firefox
   ```
   Ez a parancs leállítja az összes Firefox folyamatot.

2. **Folyamat leállítása a parancssor alapján**:
   ```bash
   pkill -f "python script.py"
   ```
   Ezzel a paranccsal leállítható minden Python folyamat, amely a `script.py` fájlt futtatja.

3. **Csak a legutoljára indított folyamat leállítása**:
   ```bash
   pkill -n ssh
   ```
   Ez a parancs csak a legutoljára indított SSH folyamatot állítja le.

4. **Jel megadása a leállításhoz**:
   ```bash
   pkill -SIGKILL process_name
   ```
   Ezzel a paranccsal a megadott folyamatot azonnal leállítja a SIGKILL jel segítségével.

## Tippek
- Mindig ellenőrizd, hogy milyen folyamatokat állítasz le, hogy elkerüld a fontos rendszerszolgáltatások leállítását.
- Használj `pgrep` parancsot a folyamatok keresésére, mielőtt a `pkill`-t használnád, hogy biztos legyél a célzott folyamatokban.
- A `-f` opció használata hasznos lehet, ha a folyamat neve nem egyértelmű, vagy ha több hasonló nevű folyamat fut.