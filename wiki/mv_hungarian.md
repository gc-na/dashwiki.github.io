# [Debian] Debian Almquist Shell (dash) mv használata: Fájlok átnevezése és áthelyezése

## Overview
A `mv` parancs a Debian Almquist Shell (dash) környezetben fájlok és könyvtárak áthelyezésére és átnevezésére szolgál. Ezzel a parancssal egyszerűen módosíthatjuk a fájlok helyét vagy nevét a fájlrendszerben.

## Usage
A `mv` parancs alapvető szintaxisa a következő:

```bash
mv [opciók] [forrás] [cél]
```

## Common Options
- `-i`: Interaktív mód, amely figyelmeztet, ha a célfájl már létezik.
- `-u`: Csak akkor mozgatja a fájlt, ha a forrás újabb, mint a célfájl, vagy ha a célfájl nem létezik.
- `-v`: Verbose (részletes) mód, amely megjeleníti a végrehajtott műveleteket.

## Common Examples
1. Fájl áthelyezése egy másik könyvtárba:
   ```bash
   mv dokumentum.txt /home/felhasználó/dokumentumok/
   ```

2. Fájl átnevezése:
   ```bash
   mv régi_név.txt új_név.txt
   ```

3. Fájl áthelyezése és átnevezése egy lépésben:
   ```bash
   mv /home/felhasználó/dokumentumok/régi_név.txt /home/felhasználó/dokumentumok/új_név.txt
   ```

4. Interaktív fájlmozgás (figyelmeztetés, ha a célfájl létezik):
   ```bash
   mv -i fájl.txt /home/felhasználó/dokumentumok/
   ```

## Tips
- Mindig ellenőrizd, hogy a célfájl létezik-e, ha nem szeretnéd felülírni.
- Használj `-v` opciót, ha szeretnéd látni, hogy pontosan mit csinál a parancs.
- A `-u` opció hasznos lehet, ha csak a legújabb fájlokat szeretnéd áthelyezni.