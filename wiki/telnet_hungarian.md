# [Debian] Debian Almquist Shell (dash) telnet használata: Hálózati kapcsolat létrehozása

## Áttekintés
A `telnet` parancs egy hálózati protokoll, amely lehetővé teszi a felhasználók számára, hogy távoli számítógépekkel létesítsenek kapcsolatot. A `telnet` segítségével parancsokat küldhetünk a távoli gépnek, és interaktív módon kommunikálhatunk vele.

## Használat
A `telnet` parancs alapvető szintaxisa a következő:

```bash
telnet [opciók] [cím] [port]
```

## Gyakori opciók
- `-l [felhasználónév]`: Bejelentkezik a megadott felhasználónévvel.
- `-d`: Debug mód, amely részletes hibakeresési információkat ad.
- `-n [fájl]`: A kimenetet a megadott fájlba irányítja.

## Gyakori példák
1. Kapcsolódás egy távoli szerverhez alapértelmezett porton (23):
   ```bash
   telnet example.com
   ```

2. Kapcsolódás egy távoli szerverhez egy adott porton (pl. 80):
   ```bash
   telnet example.com 80
   ```

3. Bejelentkezés egy távoli szerverre egy adott felhasználónévvel:
   ```bash
   telnet -l username example.com
   ```

4. Debug információk megjelenítése a kapcsolat során:
   ```bash
   telnet -d example.com
   ```

## Tippek
- A `telnet` nem titkosítja az adatokat, ezért érzékeny információk küldésére nem ajánlott.
- Használj alternatív protokollokat, mint például az SSH, ha biztonságos kapcsolatot szeretnél.
- Ellenőrizd a tűzfal beállításait, ha nem tudsz csatlakozni a távoli géphez.