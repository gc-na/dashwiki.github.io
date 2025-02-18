# [Debian] Debian Almquist Shell (dash) sed használat: Szövegfeldolgozás

## Áttekintés
A `sed` (stream editor) egy hatékony szövegfeldolgozó eszköz, amely lehetővé teszi a szöveges fájlok módosítását és manipulálását. A `sed` parancs segítségével egyszerű keresési és helyettesítési műveleteket végezhetünk, valamint komplex szövegtranszformációkat is végrehajthatunk.

## Használat
A `sed` parancs alapvető szintaxisa a következő:

```bash
sed [opciók] [argumentumok]
```

## Gyakori Opciók
- `-e`: Több `sed` parancs megadása egyetlen parancsban.
- `-f`: Parancsfájl használata, amely tartalmazza a `sed` parancsokat.
- `-i`: A fájlok közvetlen módosítása (in-place).
- `-n`: Csak a megadott kimeneteket jeleníti meg, alapértelmezés szerint nem ír ki semmit.

## Gyakori Példák
1. **Egyszerű helyettesítés**: Egy szövegfájlban az "alma" szót "banánra" cseréljük.
   ```bash
   sed 's/alma/banán/g' fájl.txt
   ```

2. **Sorok törlése**: Töröljük az összes 3. sort a fájlból.
   ```bash
   sed '3d' fájl.txt
   ```

3. **Fájl közvetlen módosítása**: Az "alma" szót "banánra" cseréljük a fájlban, és közvetlenül módosítjuk a fájlt.
   ```bash
   sed -i 's/alma/banán/g' fájl.txt
   ```

4. **Több parancs végrehajtása**: Két művelet végrehajtása egy parancsban.
   ```bash
   sed -e 's/alma/banán/g' -e 's/körte/őszibarack/g' fájl.txt
   ```

## Tippek
- Mindig készítsen biztonsági másolatot a fájlokról, mielőtt `-i` opcióval módosítaná őket.
- Használja a `-n` opciót, ha csak a módosított sorokat szeretné megjeleníteni, így elkerülheti a felesleges kimenetet.
- A reguláris kifejezések használata lehetővé teszi a bonyolultabb keresési és helyettesítési műveletek végrehajtását.