# [Debian] Debian Almquist Shell (dash) sort használata: Adatok rendezése

## Áttekintés
A `sort` parancs a fájlokban található sorokat rendezi, lehetővé téve a felhasználók számára, hogy a szöveges adatokat rendezett formában jelenítsenek meg. A rendezés alapértelmezés szerint ábécé sorrendben történik, de számos lehetőség áll rendelkezésre a rendezési kritériumok testreszabására.

## Használat
A `sort` parancs alapvető szintaxisa a következő:

```bash
sort [opciók] [argumentumok]
```

## Gyakori opciók
- `-r`: Fordított sorrendben rendezi a sorokat.
- `-n`: Számértékek szerint rendezi a sorokat.
- `-k`: Meghatározza, hogy melyik oszlop szerint történjen a rendezés.
- `-u`: Csak az egyedi sorokat tartalmazza a kimenetben.
- `-o`: A rendezett kimenetet egy megadott fájlba írja.

## Gyakori példák
1. Alapértelmezett ábécé szerinti rendezés:
   ```bash
   sort fájl.txt
   ```

2. Fordított sorrendben történő rendezés:
   ```bash
   sort -r fájl.txt
   ```

3. Számértékek szerinti rendezés:
   ```bash
   sort -n számok.txt
   ```

4. Egy adott oszlop szerint történő rendezés (például a második oszlop):
   ```bash
   sort -k 2 fájl.txt
   ```

5. Egyedi sorok kiírása:
   ```bash
   sort -u fájl.txt
   ```

6. Rendezett kimenet írása egy új fájlba:
   ```bash
   sort -o rendezett.txt fájl.txt
   ```

## Tippek
- Használj csővezetékeket (`|`) más parancsokkal a `sort` kimenetének további feldolgozásához.
- Ellenőrizd a fájlok tartalmát a `cat` paranccsal a rendezés előtt, hogy tudd, mit várhatsz el.
- A `-k` opcióval több oszlopot is megadhatsz, ha komplexebb rendezési feltételekre van szükséged.