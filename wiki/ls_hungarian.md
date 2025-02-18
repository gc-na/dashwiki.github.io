# [Debian] Debian Almquist Shell (dash) ls használat: fájlok és könyvtárak listázása

## Áttekintés
Az `ls` parancs a fájlok és könyvtárak listázására szolgál a terminálban. Segítségével könnyen megtekinthetjük a jelenlegi könyvtár tartalmát, valamint különböző információkat is kaphatunk a fájlokról.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
ls [opciók] [argumentumok]
```

## Gyakori opciók
- `-l`: Hosszú formátumban listázza a fájlokat, részletes információkkal.
- `-a`: Megjeleníti az összes fájlt, beleértve a rejtett fájlokat is (amelyek neve ponttal kezdődik).
- `-h`: Emberi olvashatóságú formátumban mutatja a fájlméreteket (pl. KB, MB).
- `-R`: Rekurzívan listázza a könyvtárakat és azok tartalmát.
- `-t`: A fájlokat módosítási idő szerint rendezi.

## Gyakori példák
1. A jelenlegi könyvtár fájljainak listázása:
   ```bash
   ls
   ```

2. A fájlok részletes listázása hosszú formátumban:
   ```bash
   ls -l
   ```

3. Az összes fájl, beleértve a rejtetteket is, megjelenítése:
   ```bash
   ls -a
   ```

4. A fájlok listázása emberi olvashatóságú méretekkel:
   ```bash
   ls -lh
   ```

5. A könyvtár rekurszív listázása:
   ```bash
   ls -R
   ```

6. A fájlok listázása módosítási idő szerint:
   ```bash
   ls -lt
   ```

## Tippek
- Használj több opciót egyszerre, például `ls -la` a részletes és rejtett fájlok megjelenítéséhez.
- A fájlok szűrésére használhatod a `grep` parancsot, például `ls | grep txt` a `.txt` fájlok keresésére.
- A `--color` opcióval színes megjelenítést érhetsz el, ami segít a fájlok gyorsabb azonosításában.