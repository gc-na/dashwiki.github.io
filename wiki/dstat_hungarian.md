# [Debian] Debian Almquist Shell (dash) dstat használata: Rendszer teljesítmény figyelése

## Áttekintés
A `dstat` parancs egy hatékony eszköz a rendszer teljesítményének valós idejű figyelésére. Segítségével különböző erőforrások, mint például a CPU, memória, lemez és hálózati aktivitás állapotát követhetjük nyomon, lehetővé téve a rendszer teljesítményének részletes elemzését.

## Használat
A `dstat` parancs alapvető szintaxisa a következő:

```bash
dstat [opciók] [argumentumok]
```

## Gyakori Opciók
- `-c`: CPU használat megjelenítése.
- `-d`: Díszk aktivitás megjelenítése.
- `-n`: Hálózati forgalom megjelenítése.
- `-m`: Memória használat megjelenítése.
- `-t`: Időbélyeg megjelenítése a kimenetben.

## Gyakori Példák
1. **Alapértelmezett dstat használat:**
   ```bash
   dstat
   ```

2. **CPU és memória használat megjelenítése:**
   ```bash
   dstat -c -m
   ```

3. **Díszk és hálózati aktivitás figyelése:**
   ```bash
   dstat -d -n
   ```

4. **Időbélyeggel ellátott teljesítményfigyelés:**
   ```bash
   dstat -t
   ```

5. **Összes erőforrás megjelenítése:**
   ```bash
   dstat -cdmn
   ```

## Tippek
- Használj több opciót egyszerre a részletesebb információkért.
- A `dstat` kimenete folyamatosan frissül, így érdemes figyelni a változásokat valós időben.
- A parancs kimenetét átirányíthatod egy fájlba, ha hosszabb távú megfigyelést szeretnél:
  ```bash
  dstat > teljesitmeny.log
  ```