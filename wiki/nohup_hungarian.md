# [Debian] Debian Almquist Shell (dash) nohup használata: Folyamatok futtatása háttérben

## Áttekintés
A `nohup` (no hang up) parancs lehetővé teszi, hogy egy parancsot vagy folyamatot háttérben futtassunk, anélkül, hogy az megszakadna, ha a felhasználó kijelentkezik a rendszerből. Ez különösen hasznos hosszú ideig futó feladatok esetén, amelyek nem igényelnek interakciót.

## Használat
A `nohup` parancs alapvető szintaxisa a következő:

```bash
nohup [opciók] [argumentumok]
```

## Gyakori Opciók
- `&` : A parancs háttérben való futtatásához használható.
- `-h` : A `nohup` használatának súgója.
- `-v` : Verbózus mód, amely részletesebb kimenetet ad.

## Gyakori Példák
1. **Egyszerű parancs háttérben történő futtatása:**
   ```bash
   nohup sleep 60 &
   ```
   Ez a parancs 60 másodpercig alszik, és a háttérben fut.

2. **Folyamat futtatása kimenet átirányításával:**
   ```bash
   nohup myscript.sh > output.log &
   ```
   A `myscript.sh` parancs kimenete az `output.log` fájlba kerül.

3. **Hosszú futású parancs indítása:**
   ```bash
   nohup python long_running_script.py &
   ```
   Ez a Python szkript a háttérben fut, és nem áll le a felhasználó kijelentkezésekor.

## Tippek
- Mindig irányítsd a kimenetet egy fájlba, hogy később ellenőrizhesd a folyamat állapotát.
- Használj `jobs` parancsot a háttérben futó folyamatok nyomon követésére.
- A `disown` parancs használatával eltávolíthatod a háttérben futó folyamatot a shellből, így az nem áll le a shell bezárásakor.