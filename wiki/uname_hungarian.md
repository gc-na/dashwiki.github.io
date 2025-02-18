# [Debian] Debian Almquist Shell (dash) uname használat: Rendszerinformációk lekérdezése

## Áttekintés
A `uname` parancs a rendszer információinak lekérdezésére szolgál, például a kernel nevét, verzióját és a gép architektúráját mutatja meg.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
uname [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Minden elérhető információt megjelenít a rendszerről.
- `-s`: A kernel nevét mutatja.
- `-n`: A gép hálózati nevét adja vissza.
- `-r`: A kernel verzióját jeleníti meg.
- `-m`: A gép architektúráját mutatja.

## Gyakori példák
1. A kernel nevét és verzióját jeleníti meg:
   ```bash
   uname -sr
   ```

2. Minden elérhető információt megjelenít:
   ```bash
   uname -a
   ```

3. A gép architektúráját adja vissza:
   ```bash
   uname -m
   ```

4. A gép hálózati nevét mutatja:
   ```bash
   uname -n
   ```

## Tippek
- Használja az `-a` opciót, ha szeretné egyszerre látni az összes fontos információt a rendszerről.
- A `uname` parancsot scriptelés során is hasznos lehet, például a rendszer architektúrájának ellenőrzésére.
- A parancs kimenete segíthet a hibaelhárításban, ha problémák merülnek fel a rendszerrel kapcsolatban.