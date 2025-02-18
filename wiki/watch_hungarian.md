# [Debian] Debian Almquist Shell (dash) watch használat: Folyamatos parancsfigyelés

## Áttekintés
A `watch` parancs lehetővé teszi, hogy egy másik parancs kimenetét folyamatosan figyeljük, frissítve azt egy meghatározott időközönként. Ez hasznos lehet például rendszerinformációk vagy fájlok állapotának nyomon követésére.

## Használat
A `watch` parancs alapvető szintaxisa a következő:

```bash
watch [opciók] [parancs]
```

## Gyakori opciók
- `-n, --interval <másodperc>`: Meghatározza a frissítési időközt másodpercekben. Alapértelmezett érték 2 másodperc.
- `-d, --differences`: Kiemeli a különbségeket a frissítések között.
- `-t, --no-title`: Elrejti a fejlécet, amely a frissítési időt és a parancsot tartalmazza.

## Gyakori példák
1. Rendszerhasználat figyelése 5 másodpercenként:
    ```bash
    watch -n 5 free -h
    ```

2. Folyamatok listázása, kiemelve a változásokat:
    ```bash
    watch -d ps aux
    ```

3. Fájlok méretének figyelése:
    ```bash
    watch -n 10 du -sh /path/to/directory
    ```

4. Hálózati kapcsolat állapotának ellenőrzése:
    ```bash
    watch -n 1 ifconfig
    ```

## Tippek
- Használj rövidebb frissítési időt, ha gyorsabb reakcióra van szükséged, de ne állítsd be túl alacsonyra, hogy elkerüld a túlzott terhelést.
- A `-d` opció használata segíthet az észlelésben, ha a kimenet nagy mennyiségű információt tartalmaz.
- Kombináld a `watch` parancsot más parancsokkal, mint például a `grep`, hogy specifikus információkat figyelj.