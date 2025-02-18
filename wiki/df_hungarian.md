# [Debian] Debian Almquist Shell (dash) df használata: lemezhasználat megjelenítése

## Áttekintés
A `df` parancs a lemezterület használatának megjelenítésére szolgál. Megmutatja, hogy a fájlrendszerek mennyi helyet használnak és mennyi szabad hely áll rendelkezésre.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
df [opciók] [argumentumok]
```

## Gyakori Opciók
- `-h`: Emberi olvasható formátumban jeleníti meg a méreteket (pl. KB, MB, GB).
- `-T`: Megjeleníti a fájlrendszer típusát is.
- `-a`: Megjeleníti az összes fájlrendszert, beleértve a nullákat is.
- `-i`: A fájlrendszer inode-jainak használatát mutatja.

## Gyakori Példák
1. Az alapvető lemezhasználat megjelenítése:
   ```bash
   df
   ```

2. Emberi olvasható formátumban:
   ```bash
   df -h
   ```

3. A fájlrendszer típusának megjelenítése:
   ```bash
   df -T
   ```

4. Az inode-ok használatának megjelenítése:
   ```bash
   df -i
   ```

5. Az összes fájlrendszer megjelenítése:
   ```bash
   df -a
   ```

## Tippek
- Használja a `-h` opciót, hogy könnyebben értelmezhető méreteket kapjon.
- Rendszeresen ellenőrizze a lemezhasználatot, hogy elkerülje a helyhiányt.
- Kombinálja az opciókat a parancsban, például: `df -h -T` a részletes és olvasható információkért.