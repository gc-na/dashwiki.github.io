# [Debian] Debian Almquist Shell (dash) pwd használat: Az aktuális könyvtár megjelenítése

## Áttekintés
A `pwd` parancs (print working directory) megjeleníti az aktuális munkakönyvtár teljes elérési útját. Ez hasznos lehet, amikor szeretnénk tudni, hogy melyik könyvtárban dolgozunk a parancssorban.

## Használat
A `pwd` parancs alapvető szintaxisa a következő:

```bash
pwd [opciók] [érvek]
```

## Gyakori opciók
- `-L`: A logikai elérési utat mutatja, amely figyelembe veszi a szimbolikus linkeket.
- `-P`: A fizikai elérési utat mutatja, amely a szimbolikus linkeket figyelmen kívül hagyja.

## Gyakori példák
1. Az aktuális könyvtár megjelenítése:
   ```bash
   pwd
   ```

2. A logikai elérési út megjelenítése:
   ```bash
   pwd -L
   ```

3. A fizikai elérési út megjelenítése:
   ```bash
   pwd -P
   ```

## Tippek
- Használja a `pwd` parancsot gyakran, hogy ellenőrizze, melyik könyvtárban dolgozik, különösen, ha több könyvtár között navigál.
- Ha szimbolikus linkekkel dolgozik, érdemes a `-P` opciót használni, hogy a valódi elérési utat lássa.