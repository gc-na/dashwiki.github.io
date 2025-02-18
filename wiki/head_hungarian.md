# [Debian] Debian Almquist Shell (dash) head használata: fájlok elejének megjelenítése

## Áttekintés
A `head` parancs a fájlok elejének megjelenítésére szolgál. Alapértelmezés szerint az első 10 sort mutatja meg, de ez módosítható különböző opciók használatával.

## Használat
A `head` parancs alapvető szintaxisa a következő:

```bash
head [opciók] [fájlok]
```

## Gyakori opciók
- `-n [szám]`: Megadja, hogy hány sort szeretnénk megjeleníteni a fájl elejéről. Például `-n 5` az első 5 sort mutatja.
- `-c [szám]`: Megadja, hogy hány bájtot szeretnénk megjeleníteni a fájl elejéről. Például `-c 100` az első 100 bájtot mutatja.
- `-q`: Csak a fájlok nevét jeleníti meg, ha több fájlt adunk meg.
- `-v`: A fájlok nevét mindig megjeleníti, függetlenül attól, hogy hány fájl van.

## Gyakori példák
1. Az első 10 sor megjelenítése egy fájlból:
   ```bash
   head fájl.txt
   ```

2. Az első 5 sor megjelenítése:
   ```bash
   head -n 5 fájl.txt
   ```

3. Az első 100 bájt megjelenítése:
   ```bash
   head -c 100 fájl.txt
   ```

4. Több fájl első 10 sorának megjelenítése:
   ```bash
   head fájl1.txt fájl2.txt
   ```

5. Az első 3 sor megjelenítése egy fájlból, a fájl nevének megjelenítésével:
   ```bash
   head -n 3 -v fájl.txt
   ```

## Tippek
- Használj `head`-et a fájlok gyors áttekintésére, hogy lásd a tartalmukat anélkül, hogy megnyitnád őket egy szövegszerkesztőben.
- Kombináld a `head` parancsot más parancsokkal, mint például a `grep`, hogy a fájlok elejéről szűrt információkat kapj.
- Ha nagy fájlokkal dolgozol, a `head` segíthet a fájlok gyors ellenőrzésében, mielőtt további műveleteket végeznél rajtuk.