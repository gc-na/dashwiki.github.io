# [Debian] Debian Almquist Shell (dash) chmod használata: Fájlok jogosultságainak módosítása

## Áttekintés
A `chmod` parancs a fájlok és könyvtárak jogosultságainak módosítására szolgál a Unix-alapú operációs rendszerekben, beleértve a Debian Almquist Shell (dash) környezetet is. Ezzel a paranccsal beállíthatjuk, hogy ki férhet hozzá a fájlokhoz, és milyen műveleteket végezhet el rajtuk.

## Használat
A `chmod` parancs alapvető szintaxisa a következő:

```bash
chmod [opciók] [argumentumok]
```

## Gyakori opciók
- `-R`: Rekurzív módon alkalmazza a jogosultságokat a megadott könyvtárra és annak összes almappájára.
- `u`: A fájl tulajdonosának jogosultságait módosítja.
- `g`: A fájl csoportjának jogosultságait módosítja.
- `o`: A fájl egyéb felhasználóinak jogosultságait módosítja.
- `+`: Jogosultság hozzáadása.
- `-`: Jogosultság eltávolítása.
- `=`: Jogosultságok beállítása.

## Gyakori példák
- A fájl olvasási jogosultságának hozzáadása a tulajdonoshoz:
```bash
chmod u+r fájl.txt
```

- A fájl írási jogosultságának eltávolítása a csoportból:
```bash
chmod g-w fájl.txt
```

- A fájl végrehajtási jogosultságának beállítása minden felhasználónak:
```bash
chmod a+x fájl.txt
```

- Rekurzív jogosultságok módosítása egy könyvtárban:
```bash
chmod -R 755 könyvtár/
```

## Tippek
- Mindig ellenőrizd a fájl jogosultságait a `ls -l` paranccsal a módosítások előtt és után.
- Használj rekurzív módot óvatosan, hogy elkerüld a nem kívánt jogosultságok beállítását.
- A jogosultságok numerikus formátumban (pl. 755) történő megadása gyorsabb lehet, mint a betűszavak használata.