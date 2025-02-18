# [Debian] Debian Almquist Shell (dash) pidstat használata: Folyamat statisztikák megjelenítése

## Áttekintés
A `pidstat` parancs a rendszerfolyamatok statisztikáinak megjelenítésére szolgál, lehetővé téve a felhasználók számára, hogy nyomon követhessék a CPU és memóriahasználatot, valamint más teljesítménymutatókat egy vagy több folyamat esetében.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
pidstat [opciók] [érvek]
```

## Gyakori opciók
- `-h`: A fejléc megjelenítése a kimenetben.
- `-r`: A memóriahasználat megjelenítése.
- `-u`: A CPU használat megjelenítése.
- `-p <PID>`: Csak a megadott folyamat azonosítójú folyamat statisztikáit mutatja.
- `-t`: A szálak statisztikáinak megjelenítése.

## Gyakori példák
1. **Alapvető folyamat statisztikák megjelenítése:**
   ```bash
   pidstat
   ```

2. **Csak a CPU használat megjelenítése:**
   ```bash
   pidstat -u
   ```

3. **Memóriahasználat megjelenítése:**
   ```bash
   pidstat -r
   ```

4. **Egy adott PID statisztikáinak megjelenítése:**
   ```bash
   pidstat -p 1234
   ```

5. **Szálak statisztikáinak megjelenítése:**
   ```bash
   pidstat -t
   ```

## Tippek
- Használja a `-h` opciót, hogy könnyebben olvasható fejlécet kapjon a kimenetben.
- A `pidstat` parancsot érdemes cron ütemezett feladatként futtatni a rendszer teljesítményének folyamatos nyomon követésére.
- Kombinálja a `pidstat`-ot más parancsokkal, mint például a `grep`, hogy szűkítse a kimenetet egy adott folyamatra.