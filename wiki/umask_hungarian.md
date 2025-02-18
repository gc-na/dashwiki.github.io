# [Debian] Debian Almquist Shell (dash) umask használata: fájlok alapértelmezett jogosultságainak beállítása

## Áttekintés
A `umask` parancs a fájlok és könyvtárak alapértelmezett jogosultságainak beállítására szolgál a Unix-alapú rendszerekben. A `umask` érték határozza meg, hogy a létrehozott fájlok és könyvtárak milyen jogosultságokkal rendelkezzenek.

## Használat
A `umask` parancs alapvető szintaxisa a következő:

```bash
umask [opciók] [érvek]
```

## Gyakori Opciók
- `-S`: Megjeleníti a jogosultságokat szimbolikus formában.
- `-p`: Megjeleníti a jelenlegi umask értéket.
- `-c`: Beállítja a megadott umask értéket, és visszaállítja az előző értéket.

## Gyakori Példák
1. A jelenlegi umask érték megjelenítése:
   ```bash
   umask
   ```

2. A umask érték beállítása 022-re (a fájlok alapértelmezett jogosultságai 644, a könyvtáraké 755):
   ```bash
   umask 022
   ```

3. A jogosultságok szimbolikus formában való megjelenítése:
   ```bash
   umask -S
   ```

4. A umask érték ideiglenes beállítása 007-re:
   ```bash
   umask 007
   ```

## Tippek
- A `umask` parancsot általában a felhasználói profil fájlokban (pl. `.bashrc`, `.profile`) érdemes beállítani, hogy a kívánt alapértelmezett jogosultságok mindig érvényesüljenek.
- Ellenőrizd a `umask` értékedet a fájlok létrehozása előtt, hogy biztos lehess benne, hogy a kívánt jogosultságok érvényesülnek.
- Használj szimbolikus formát a jogosultságok gyorsabb és érthetőbb beállításához.