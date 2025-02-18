# [Debian] Debian Almquist Shell (dash) find használat: fájlok keresése

## Áttekintés
A `find` parancs lehetővé teszi fájlok és könyvtárak keresését a fájlrendszerben különböző kritériumok alapján, mint például név, típus, méret vagy módosítási idő.

## Használat
A `find` parancs alapvető szintaxisa a következő:

```bash
find [opciók] [érvek]
```

## Gyakori Opciók
- `-name`: Keresés fájlnevek alapján.
- `-type`: Keresés fájltípus alapján (pl. `f` fájl, `d` könyvtár).
- `-size`: Keresés fájlméret alapján.
- `-mtime`: Keresés a fájl utolsó módosítási ideje alapján.
- `-exec`: Parancs végrehajtása a megtalált fájlokon.

## Gyakori Példák
1. Fájlok keresése név alapján:
   ```bash
   find /path/to/directory -name "file.txt"
   ```

2. Minden könyvtár keresése a megadott helyen:
   ```bash
   find /path/to/directory -type d
   ```

3. Fájlok keresése, amelyek nagyobbak 1 MB-nál:
   ```bash
   find /path/to/directory -size +1M
   ```

4. Fájlok keresése, amelyeket az utolsó 7 napban módosítottak:
   ```bash
   find /path/to/directory -mtime -7
   ```

5. Parancs végrehajtása a megtalált fájlokon:
   ```bash
   find /path/to/directory -name "*.log" -exec rm {} \;
   ```

## Tippek
- Használj relatív vagy abszolút elérési utakat a pontosabb keresés érdekében.
- A `-print` opció alapértelmezett, de használhatod kifejezetten, ha más opciókat is használsz.
- A `-maxdepth` opcióval korlátozhatod a keresés mélységét, hogy ne keresgélj túl mélyen a fájlrendszerben.