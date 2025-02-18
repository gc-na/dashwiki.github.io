# [Debian] Debian Almquist Shell (dash) cd használata: Mappa váltás

## Áttekintés
A `cd` parancs a Debian Almquist Shell (dash) környezetében a munkakönyvtár (aktuális mappa) megváltoztatására szolgál. Ezzel a parancssal navigálhatunk a fájlrendszer különböző könyvtárai között.

## Használat
A `cd` parancs alapvető szintaxisa a következő:

```bash
cd [opciók] [érvek]
```

## Gyakori Opciók
- `-`: Visszalép a legutolsó könyvtárba.
- `..`: A szülő könyvtárba lép.
- `~`: A felhasználó otthoni könyvtárába lép.

## Gyakori Példák
1. **Váltás a felhasználó otthoni könyvtárába:**
   ```bash
   cd ~
   ```

2. **Váltás a szülő könyvtárba:**
   ```bash
   cd ..
   ```

3. **Váltás egy konkrét könyvtárba:**
   ```bash
   cd /path/to/directory
   ```

4. **Visszalépés a legutolsó könyvtárba:**
   ```bash
   cd -
   ```

## Tippek
- Használja a `tab` billentyűt a könyvtárnevek automatikus kiegészítéséhez, így gyorsabban navigálhat.
- Ellenőrizze az aktuális könyvtárat a `pwd` parancs használatával, hogy mindig tudja, hol tartózkodik a fájlrendszerben.
- Ha gyakran használ egy adott könyvtárat, érdemes lehet egy alias-t létrehozni, hogy gyorsabban elérhesse.