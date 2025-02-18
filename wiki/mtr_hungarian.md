# [Debian] Debian Almquist Shell (dash) mtr használat: Hálózati útvonalak nyomkövetése

## Áttekintés
A mtr (My Traceroute) parancs egy hálózati diagnosztikai eszköz, amely kombinálja a traceroute és a ping parancsok funkcióit. Segítségével nyomon követhetjük a hálózati útvonalakat és ellenőrizhetjük a csomagok késleltetését a célállomásig.

## Használat
A mtr parancs alapvető szintaxisa a következő:

```bash
mtr [opciók] [cél]
```

## Gyakori opciók
- `-r` : Jelentés generálása, amely a parancs végrehajtása után azonnal megjeleníti az eredményeket.
- `-c <szám>` : Megadja, hogy hány ping kérést küldjön a mtr.
- `-n` : Ne fordítsa le a címeket DNS név alapján, csak IP címeket mutasson.
- `-p` : A mtr parancs futtatása port megadásával.

## Gyakori példák
1. Alapértelmezett mtr futtatás egy cél IP címmel:
   ```bash
   mtr 8.8.8.8
   ```

2. Mtr futtatása jelentés generálásával:
   ```bash
   mtr -r 8.8.8.8
   ```

3. Mtr futtatása egy adott számú ping kéréssel:
   ```bash
   mtr -c 10 8.8.8.8
   ```

4. Mtr futtatása DNS név feloldás nélkül:
   ```bash
   mtr -n google.com
   ```

## Tippek
- Használj `-r` opciót, ha gyorsan szeretnél egy jelentést kapni az útvonalról.
- A `-n` opció használata gyorsabbá teheti a parancsot, ha nem szükséges a DNS név feloldás.
- Figyeld a csomagok késleltetését és a veszteséget, hogy azonosíthasd a hálózati problémákat.