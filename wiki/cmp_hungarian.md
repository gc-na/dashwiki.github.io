# [Debian] Debian Almquist Shell (dash) cmp használata: Fájlok összehasonlítása

## Áttekintés
A `cmp` parancs arra szolgál, hogy összehasonlítsa két fájl tartalmát byte szinten. Ha eltérést talál, megjeleníti a különbség helyét, így segít a fájlok közötti eltérések azonosításában.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
cmp [opciók] [fájl1] [fájl2]
```

## Gyakori opciók
- `-l`: Minden eltérést listáz, byte-onként.
- `-s`: Csendes mód, csak a visszatérési kódot adja meg, eltérés esetén.
- `-i OFFSET`: Az összehasonlítást az OFFSET byte-tól kezdi.

## Gyakori példák
- Két fájl egyszerű összehasonlítása:

```bash
cmp file1.txt file2.txt
```

- Eltérések listázása byte-onként:

```bash
cmp -l file1.txt file2.txt
```

- Csendes összehasonlítás, csak a visszatérési kód:

```bash
cmp -s file1.txt file2.txt
```

- Összehasonlítás OFFSET-től kezdve:

```bash
cmp -i 10 file1.txt file2.txt
```

## Tippek
- Használj `-s` opciót, ha csak a fájlok eltérésének létezésére vagy kíváncsi, anélkül, hogy a részletek érdekelnének.
- A `-l` opció hasznos lehet, ha pontosan tudni szeretnéd, hogy mely byte-ok térnek el.
- Ellenőrizd a visszatérési kódot a parancs futtatása után, hogy megtudd, a fájlok azonosak-e (0), eltérnek (1), vagy ha hiba történt (2).