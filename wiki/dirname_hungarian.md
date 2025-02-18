# [Debian] Debian Almquist Shell (dash) dirname használata: A fájlok elérési útjának kinyerése

## Áttekintés
A `dirname` parancs a fájlok elérési útjának kinyerésére szolgál. A megadott fájlnevek alapján visszaadja a fájlok szülőkönyvtárának nevét, így segít a fájlok helyének meghatározásában.

## Használat
A `dirname` parancs alapvető szintaxisa a következő:

```bash
dirname [opciók] [argumentumok]
```

## Gyakori opciók
- Nincs különösebb opció, a `dirname` parancs alapvetően a megadott argumentumokkal működik.

## Gyakori példák
1. A fájl elérési útjának kinyerése:
   ```bash
   dirname /home/felhasználó/dokumentumok/fájl.txt
   ```
   Kimenet:
   ```
   /home/felhasználó/dokumentumok
   ```

2. Több fájl elérési útjának kinyerése:
   ```bash
   dirname /usr/local/bin/script.sh
   dirname /var/log/syslog
   ```
   Kimenet:
   ```
   /usr/local/bin
   /var/log
   ```

3. A jelenlegi könyvtárban található fájl elérési útjának kinyerése:
   ```bash
   dirname ./fájl.txt
   ```
   Kimenet:
   ```
   .
   ```

## Tippek
- Használja a `dirname` parancsot szkriptekben, hogy dinamikusan kinyerje a fájlok elérési útját.
- Kombinálja a `dirname` parancsot más parancsokkal, mint például a `find` vagy a `xargs`, hogy hatékonyabban kezelje a fájlokat.
- Ellenőrizze a kimenetet, hogy megbizonyosodjon arról, hogy a várt elérési utat kapta, különösen, ha szimbolikus linkekkel dolgozik.