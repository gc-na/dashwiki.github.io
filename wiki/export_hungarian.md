# [Debian] Debian Almquist Shell (dash) export használata: Környezeti változók beállítása

## Áttekintés
Az `export` parancs a Debian Almquist Shell (dash) környezetében lehetővé teszi a környezeti változók beállítását, amelyeket a shell és az alárendelt folyamatok is használnak. Ezzel a paranccsal megoszthatjuk a változókat más programokkal, amelyek a shellből indulnak.

## Használat
A parancs alapvető szintaxisa a következő:

```sh
export [opciók] [változó=érték]
```

## Gyakori opciók
- `-p`: Megjeleníti az összes exportált változót.
- `Változó=érték`: Beállít egy új környezeti változót a megadott értékkel.

## Gyakori példák
1. **Környezeti változó létrehozása**:
   ```sh
   export MY_VAR="Hello, World!"
   ```

2. **Környezeti változó megjelenítése**:
   ```sh
   echo $MY_VAR
   ```

3. **Több változó egyidejű exportálása**:
   ```sh
   export VAR1="Value1" VAR2="Value2"
   ```

4. **Exportált változók listázása**:
   ```sh
   export -p
   ```

## Tippek
- Mindig ellenőrizd, hogy a változókat helyesen exportálod-e, különben nem lesznek elérhetők az alárendelt folyamatok számára.
- Használj egyértelmű és leíró neveket a változókhoz, hogy könnyen azonosíthatók legyenek.
- A változók értékének megadásakor figyelj a szóközökre; például `export VAR="value"` helyett `export VAR = "value"` nem működik.