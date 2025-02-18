# [Debian] Debian Almquist Shell (dash) trap használat: Jelek kezelése

## Áttekintés
A `trap` parancs lehetővé teszi, hogy a shell parancsok jeleket (signal) kezeljen. Ezzel a parancssal megadhatjuk, hogy a shell hogyan reagáljon bizonyos jelekre, például amikor a felhasználó megszakítja a futó folyamatot.

## Használat
A `trap` parancs alapvető szintaxisa a következő:

```sh
trap [opciók] [argumentumok]
```

## Gyakori opciók
- `SIGINT`: A megszakítási jel, amelyet a Ctrl+C kombinációval küldünk.
- `SIGTERM`: A leállítási jel, amelyet a folyamatok leállítására használnak.
- `EXIT`: A parancs végrehajtásának befejezésekor végrehajtandó műveletek.

## Gyakori példák
1. **Alapvető jelkezelés**:
   A következő példa megakadályozza, hogy a Ctrl+C megszakítsa a scriptet, és helyette egy üzenetet ír ki.
   ```sh
   trap 'echo "A folyamat megszakítva!"' SIGINT
   while true; do
       echo "Folyamat fut..."
       sleep 1
   done
   ```

2. **Folyamat leállítása**:
   Itt a `trap` parancs leállítja a folyamatot, amikor a SIGTERM jelet kapja.
   ```sh
   trap 'echo "Folyamat leállítva!"; exit' SIGTERM
   while true; do
       echo "Folyamat fut..."
       sleep 1
   done
   ```

3. **Takarítás a script befejezésekor**:
   A következő példa megmutatja, hogyan lehet takarító műveleteket végezni a script befejezésekor.
   ```sh
   trap 'echo "Takarítás folyamatban..."; rm -f temp.txt' EXIT
   touch temp.txt
   echo "Folyamat fut..."
   ```

## Tippek
- Mindig érdemes jeleket kezelni, hogy a scriptjeid ne hagyjanak hátra felesleges fájlokat vagy erőforrásokat.
- Használj világos üzeneteket a `trap` parancsban, hogy a felhasználók tudják, mi történik, ha megszakítják a folyamatot.
- Teszteld a scriptjeidet különböző jelek küldésével, hogy megbizonyosodj arról, hogy a `trap` megfelelően működik.