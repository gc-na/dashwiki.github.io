# [Debian] Debian Almquist Shell (dash) strace használata: Rendszerhívások nyomkövetése

## Áttekintés
A `strace` parancs egy hasznos eszköz, amely lehetővé teszi a programok által végrehajtott rendszerhívások és jelek nyomon követését. Segítségével részletes információkat kaphatunk arról, hogy egy adott program hogyan kommunikál a kernel-lel, ami segíthet a hibakeresésben és a teljesítmény optimalizálásában.

## Használat
A `strace` parancs alapvető szintaxisa a következő:

```bash
strace [opciók] [argumentumok]
```

## Gyakori opciók
- `-c`: Összegzi a rendszerhívásokat és statisztikákat ad vissza.
- `-f`: Követi a forkolt folyamatokat is.
- `-o <fájl>`: Az összes kimenetet egy megadott fájlba irányítja.
- `-e <kifejezés>`: Csak a megadott rendszerhívásokat követi.
- `-p <PID>`: Egy már futó folyamatot követ.

## Gyakori példák
1. **Alapvető használat**: Egy program rendszerhívásainak nyomon követése.
   ```bash
   strace ls
   ```

2. **Kimenet fájlba írása**: A `ls` parancs rendszerhívásainak mentése egy fájlba.
   ```bash
   strace -o strace_output.txt ls
   ```

3. **Forkolt folyamatok követése**: A `grep` parancs nyomkövetése, beleértve a forkolt folyamatokat is.
   ```bash
   strace -f grep "valami" fájl.txt
   ```

4. **Csak bizonyos rendszerhívások követése**: Például csak a `open` és `close` hívások nyomon követése.
   ```bash
   strace -e trace=open,close ls
   ```

5. **Folyamat követése PID alapján**: Egy már futó folyamat nyomkövetése a PID-jével.
   ```bash
   strace -p 1234
   ```

## Tippek
- Használja a `-c` opciót, ha szeretné gyorsan áttekinteni a rendszerhívások statisztikáit.
- A `-o` opcióval könnyen dokumentálhatja a nyomkövetési eredményeket, így később is visszanézheti őket.
- A `-f` opció különösen hasznos, ha a program fork-okat használ, mivel így láthatja a gyermek folyamatok hívásait is.
- Ne feledje, hogy a `strace` használata lassíthatja a program futását, így érdemes csak akkor használni, ha valóban szükséges.