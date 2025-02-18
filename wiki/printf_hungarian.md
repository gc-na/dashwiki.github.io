# [Debian] Debian Almquist Shell (dash) printf használata: Szöveg formázása és kiírása

## Áttekintés
A `printf` parancs a Debian Almquist Shell (dash) környezetében formázott szöveg kiírására szolgál. Lehetővé teszi a felhasználók számára, hogy a kimenetet pontosan úgy formázzák, ahogyan azt szeretnék, például számok, szövegek és egyéb adatok megjelenítésekor.

## Használat
A `printf` parancs alapvető szintaxisa a következő:

```sh
printf [opciók] [formátum] [argumentumok]
```

## Gyakori opciók
- `-v`: A kimenetet egy változóba menti ahelyett, hogy a standard kimenetre írna.
- `-f`: A formátumot megadja, amely szerint a kimenet készül.
- `--help`: Megjeleníti a parancs használatával kapcsolatos információkat.

## Gyakori példák
1. Egyszerű szöveg kiírása:
   ```sh
   printf "Helló, világ!\n"
   ```

2. Számok formázása:
   ```sh
   printf "A szám: %d\n" 42
   ```

3. Tizedesjegyek megjelenítése:
   ```sh
   printf "A pi értéke: %.2f\n" 3.14159
   ```

4. Több argumentum kiírása:
   ```sh
   printf "Név: %s, Kor: %d\n" "János" 30
   ```

5. Változóba mentés:
   ```sh
   printf -v myvar "A változó értéke: %d" 100
   echo "$myvar"
   ```

## Tippek
- Használj formátum specifikátorokat a kimenet pontosabb vezérléséhez.
- Ellenőrizd a kimenetet, hogy megbizonyosodj arról, hogy a formázás megfelel az elvárásaidnak.
- A `\n` karaktert használd új sorok létrehozásához a kimenetben.