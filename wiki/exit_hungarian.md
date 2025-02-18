# [Debian] Debian Almquist Shell (dash) exit használat: A shell kilépése

## Overview
Az `exit` parancs a Debian Almquist Shell (dash) környezetben a shell vagy a script futásának befejezésére szolgál. Ezzel a paranccsal megadhatjuk, hogy a shell milyen státusz kóddal záruljon le.

## Usage
A `exit` parancs alapvető szintaxisa a következő:

```sh
exit [options] [status]
```

## Common Options
- `status`: Egy egész szám, amely a shell kilépési státuszát jelöli. Alapértelmezés szerint 0, ami a sikeres végrehajtást jelenti.

## Common Examples
1. **Alapértelmezett kilépés**:
   A shell bezárása alapértelmezett státusz kóddal (0):
   ```sh
   exit
   ```

2. **Kilépés egy adott státusz kóddal**:
   A shell bezárása 1-es státusz kóddal, amely hibát jelez:
   ```sh
   exit 1
   ```

3. **Kilépés egy scriptből**:
   Egy script végén a `exit` parancs használata a script sikeres befejezéséhez:
   ```sh
   #!/bin/dash
   echo "A script futása befejeződött."
   exit 0
   ```

4. **Hiba esetén való kilépés**:
   Ha egy parancs nem sikerül, a script azonnali leállítása:
   ```sh
   #!/bin/dash
   cp nem_letező_fajl.txt cél_fajl.txt || exit 1
   ```

## Tips
- Mindig érdemes megadni a kilépési státuszt, hogy más parancsok vagy script-ek tudják, hogy a végrehajtás sikeres volt-e.
- A 0 státusz kód a sikeres végrehajtást jelzi, míg a 1 vagy annál nagyobb kódok hibát jeleznek.
- A `exit` parancs használata a script végén segít a hibák nyomon követésében és a programok helyes működésének biztosításában.