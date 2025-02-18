# [Debian] Debian Almquist Shell (dash) top használata: Rendszerfolyamatok megjelenítése

## Áttekintés
A `top` parancs egy interaktív eszköz, amely valós időben mutatja a rendszerfolyamatokat és azok erőforrás-használatát. Segítségével könnyen nyomon követhetjük a CPU, memória és egyéb erőforrások kihasználtságát.

## Használat
A `top` parancs alapvető szintaxisa a következő:

```bash
top [opciók] [argumentumok]
```

## Gyakori opciók
- `-d <másodperc>`: Beállítja a frissítési időtartamot másodpercekben.
- `-n <szám>`: Megadja, hogy hányszor frissítse a megjelenítést, majd kilép.
- `-u <felhasználónév>`: Csak a megadott felhasználó folyamatainak megjelenítése.

## Gyakori példák
1. A `top` parancs egyszerű futtatása:
   ```bash
   top
   ```

2. A frissítési időtartam beállítása 5 másodpercre:
   ```bash
   top -d 5
   ```

3. Csak egy adott felhasználó folyamatainak megjelenítése:
   ```bash
   top -u felhasználónév
   ```

4. A `top` parancs futtatása, amely 10 frissítést követően kilép:
   ```bash
   top -n 10
   ```

## Tippek
- Használja a `h` billentyűt a `top` felületen a súgó megjelenítéséhez, amely bemutatja a különböző billentyűparancsokat.
- A folyamatok rendezéséhez használja az `Shift + P` (CPU használat) vagy az `Shift + M` (memória használat) billentyűkombinációkat.
- A `k` billentyűt használva kiléphet egy folyamatot, ha megadja a folyamat azonosítóját (PID).