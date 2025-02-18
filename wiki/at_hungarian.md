# [Debian] Debian Almquist Shell (dash) at: Ütemezett parancsok futtatása

## Áttekintés
Az `at` parancs lehetővé teszi, hogy egy adott időpontban ütemezett parancsokat futtassunk a rendszerben. Használatával egyszerűen beállíthatunk feladatokat, amelyek automatikusan végrehajtódnak a megadott időben.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
at [opciók] [argumentumok]
```

## Gyakori opciók
- `-f` : Fájl megadása, amely tartalmazza a végrehajtandó parancsokat.
- `-m` : E-mail értesítést küld a felhasználónak, ha a parancs végrehajtása befejeződött.
- `-q` : Megadja a sorozatszámot, amelyben a feladatot végrehajtják (pl. `a`, `b`, `c`).
- `-l` : Megjeleníti a felhasználó által ütemezett feladatokat.

## Gyakori példák
1. **Egyszerű parancs ütemezése**
   ```bash
   echo "Hello, World!" | at now + 1 minute
   ```

2. **Parancsfájl futtatása egy adott időpontban**
   ```bash
   at 14:00 -f /path/to/script.sh
   ```

3. **E-mail értesítés beállítása**
   ```bash
   echo "Backup completed" | at now + 2 hours -m
   ```

4. **Feladatok listázása**
   ```bash
   atq
   ```

5. **Feladat törlése**
   ```bash
   atrm 1
   ```

## Tippek
- Mindig ellenőrizd az ütemezett feladatokat az `atq` paranccsal, hogy elkerüld a duplikált ütemezéseket.
- Használj e-mail értesítést, ha fontos, hogy értesülj a parancsok végrehajtásáról.
- Ügyelj arra, hogy a parancsok és fájlok elérhetők legyenek a megadott időpontban, különben a feladat nem fog végrehajtódni.