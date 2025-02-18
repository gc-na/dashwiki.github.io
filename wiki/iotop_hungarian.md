# [Debian] Debian Almquist Shell (dash) iotop használata: A lemezhasználat figyelése

## Áttekintés
Az `iotop` parancs egy hasznos eszköz a Linux rendszerek számára, amely lehetővé teszi a lemezhasználat valós idejű figyelését. Segítségével nyomon követhetjük, hogy mely folyamatok használják a legnagyobb I/O erőforrásokat, így könnyen azonosíthatjuk a teljesítményproblémákat.

## Használat
A `iotop` parancs alapvető szintaxisa a következő:

```bash
iotop [opciók] [argumentumok]
```

## Gyakori opciók
- `-o` vagy `--only`: Csak az I/O-t végző folyamatokat mutatja.
- `-b` vagy `--batch`: Batch módban fut, amely lehetővé teszi a kimenet fájlba írását.
- `-n NUM`: Meghatározza, hogy hány frissítést végezzen a batch módban.
- `-d SEC`: Beállítja a frissítési időközt másodpercekben.

## Gyakori példák
1. **Alapértelmezett használat**:
   Az `iotop` egyszerű futtatása a lemezhasználat valós idejű megjelenítéséhez:
   ```bash
   iotop
   ```

2. **Csak az I/O-t végző folyamatok megjelenítése**:
   Az alábbi parancs csak az aktívan I/O-t végző folyamatokat mutatja:
   ```bash
   iotop -o
   ```

3. **Batch módban történő futtatás**:
   Az alábbi példa batch módban futtatja az `iotop`-ot, 5 másodperces frissítési időközönként, és 10 frissítést végez:
   ```bash
   iotop -b -n 10 -d 5
   ```

4. **Kimenet fájlba írása**:
   A következő parancs a kimenetet egy fájlba irányítja:
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

## Tippek
- Használja az `-o` opciót, ha csak az aktívan I/O-t végző folyamatokra kíváncsi, így tisztább képet kap a rendszer terheltségéről.
- A batch mód hasznos lehet, ha automatizált jelentéseket szeretne készíteni a lemezhasználatról.
- Figyelje meg a legnagyobb I/O-t végző folyamatokat, és ha szükséges, optimalizálja azokat a teljesítmény javítása érdekében.