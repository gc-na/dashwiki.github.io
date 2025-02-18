# [Debian] Debian Almquist Shell (dash) zip használat: Fájlok tömörítése

## Áttekintés
A `zip` parancs lehetővé teszi fájlok és mappák tömörítését egyetlen tömörített fájlba, amelyet könnyen tárolhatunk vagy megoszthatunk. A zip formátum széles körben használt, és támogatja a tömörített fájlok gyors kicsomagolását is.

## Használat
A `zip` parancs alapvető szintaxisa a következő:

```sh
zip [opciók] [fájlok]
```

## Gyakori opciók
- `-r`: Rekurzívan tömöríti a mappákat.
- `-e`: Titkosítja a zip fájlt.
- `-9`: Maximális tömörítési szintet alkalmaz.
- `-d`: Fájlok eltávolítása a zip fájlból.

## Gyakori példák
1. **Egyszerű fájl tömörítése:**
   ```sh
   zip myarchive.zip file1.txt file2.txt
   ```

2. **Mappa tömörítése rekurzívan:**
   ```sh
   zip -r myarchive.zip myfolder/
   ```

3. **Titkosított zip fájl létrehozása:**
   ```sh
   zip -e mysecurearchive.zip file1.txt
   ```

4. **Fájl eltávolítása a zip fájlból:**
   ```sh
   zip -d myarchive.zip file1.txt
   ```

## Tippek
- Mindig használj megfelelő opciókat a tömörítési szint és a titkosítás érdekében.
- A zip fájlok kicsomagolásához használhatod a `unzip` parancsot.
- Ha nagy fájlokat tömörítesz, érdemes a `-9` opciót használni a maximális tömörítés érdekében, de ez több időt vehet igénybe.