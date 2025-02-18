# [Debian] Debian Almquist Shell (dash) basename használata: fájlnevek egyszerűsítése

## Áttekintés
A `basename` parancs a fájlnevek egyszerűsítésére szolgál, eltávolítva a megadott fájl elérési útvonalát, így csak a fájl neve marad.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
basename [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Több fájlnevet is megadhatunk, és a parancs mindegyikre alkalmazni fogja a műveletet.
- `-s`: Eltávolít egy megadott kiterjesztést a fájlnévből.

## Gyakori példák
1. Egyszerű fájlnév lekérése:
   ```bash
   basename /home/user/file.txt
   ```
   Kimenet: `file.txt`

2. Fájlnév kiterjesztésének eltávolítása:
   ```bash
   basename /home/user/file.txt .txt
   ```
   Kimenet: `file`

3. Több fájlnév egyszerre:
   ```bash
   basename -a /home/user/file1.txt /home/user/file2.txt
   ```
   Kimenet:
   ```
   file1.txt
   file2.txt
   ```

4. Kiterjesztés eltávolítása több fájlnévből:
   ```bash
   basename -a /home/user/file1.txt /home/user/file2.txt .txt
   ```
   Kimenet:
   ```
   file1
   file2
   ```

## Tippek
- Használja a `-s` opciót, ha csak a fájl kiterjesztését szeretné eltávolítani, anélkül, hogy a teljes elérési utat meg kellene adnia.
- A `basename` parancsot gyakran használják szkriptekben, ahol a fájlnevek egyszerűsítése szükséges a további feldolgozáshoz.
- Ha több fájlt szeretne kezelni, a `-a` opcióval egyszerre több fájlnevet is megadhat, így időt takaríthat meg.