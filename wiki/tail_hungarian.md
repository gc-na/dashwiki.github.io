# [Debian] Debian Almquist Shell (dash) tail használata: A fájlok végének megjelenítése

## Áttekintés
A `tail` parancs a fájlok végén található sorokat jeleníti meg. Alapértelmezés szerint az utolsó 10 sort mutatja, de a felhasználó igényei szerint testre szabható.

## Használat
A `tail` parancs alapvető szintaxisa a következő:

```bash
tail [opciók] [argumentumok]
```

## Gyakori opciók
- `-n [szám]`: Megadja, hogy hány sort szeretnénk megjeleníteni a fájl végéről.
- `-f`: Folyamatosan figyeli a fájlt, és megjeleníti az új sorokat, amint hozzáadódnak.
- `-c [szám]`: A fájl végéről a megadott bájtok számát jeleníti meg.

## Gyakori példák
1. Az utolsó 10 sor megjelenítése egy fájlból:
   ```bash
   tail fájlneve.txt
   ```

2. Az utolsó 20 sor megjelenítése:
   ```bash
   tail -n 20 fájlneve.txt
   ```

3. Folyamatos figyelés egy naplófájl esetén:
   ```bash
   tail -f naplo.log
   ```

4. Az utolsó 50 bájt megjelenítése:
   ```bash
   tail -c 50 fájlneve.txt
   ```

## Tippek
- Használja a `-f` opciót, ha naplófájlokat figyel, hogy azonnal láthassa az új bejegyzéseket.
- Kombinálja a `tail` parancsot más parancsokkal, mint például a `grep`, hogy csak a releváns sorokat jelenítse meg.
- A `tail` parancsot hasznos lehet automatizált szkriptekben is, ahol a fájlok végén található információkra van szükség.