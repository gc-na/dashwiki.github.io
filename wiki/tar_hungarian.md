# [Debian] Debian Almquist Shell (dash) tar használata: fájlok tömörítése és kicsomagolása

## Áttekintés
A `tar` parancs a fájlok és könyvtárak tömörítésére és archiválására szolgál a Unix-alapú rendszerekben. A `tar` lehetővé teszi, hogy több fájlt egyetlen fájlba csomagoljunk, amelyet gyakran `.tar` kiterjesztéssel mentenek el.

## Használat
A `tar` parancs alapvető szintaxisa a következő:

```bash
tar [opciók] [argumentumok]
```

## Gyakori opciók
- `-c`: Új archívum létrehozása.
- `-x`: Archívum kicsomagolása.
- `-f`: Az archívum fájlnevének megadása.
- `-v`: Részletes kimenet, amely megmutatja a feldolgozott fájlokat.
- `-z`: Gzip tömörítéssel való használat.
- `-j`: Bzip2 tömörítéssel való használat.

## Gyakori példák

### Archívum létrehozása
Egy könyvtár tömörítése egy `.tar` fájlba:

```bash
tar -cvf archive.tar /path/to/directory
```

### Archívum kicsomagolása
Egy `.tar` fájl kicsomagolása:

```bash
tar -xvf archive.tar
```

### Gzip tömörítés használata
Egy könyvtár tömörítése gzip segítségével:

```bash
tar -czvf archive.tar.gz /path/to/directory
```

### Gzip tömörítés kicsomagolása
Gzip tömörített archívum kicsomagolása:

```bash
tar -xzvf archive.tar.gz
```

### Bzip2 tömörítés használata
Egy könyvtár tömörítése bzip2 segítségével:

```bash
tar -cjvf archive.tar.bz2 /path/to/directory
```

### Bzip2 tömörítés kicsomagolása
Bzip2 tömörített archívum kicsomagolása:

```bash
tar -xjvf archive.tar.bz2
```

## Tippek
- Mindig használj `-v` opciót, ha szeretnéd látni, hogy mely fájlok kerülnek feldolgozásra.
- Tömörítés előtt érdemes ellenőrizni a könyvtár tartalmát a `ls` paranccsal.
- Az archívumok neveit érdemes egyértelműen megválasztani, hogy később könnyen azonosíthatók legyenek.