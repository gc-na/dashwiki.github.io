# [Debian] Debian Almquist Shell (dash) test használat: Fájlok és feltételek ellenőrzése

## Overview
A `test` parancs a fájlok és feltételek ellenőrzésére szolgál a shell környezetben. Segítségével különböző logikai és fájl állapotokat vizsgálhatunk meg, mint például, hogy egy fájl létezik-e, vagy hogy egy szám nagyobb-e egy másik számnál.

## Usage
A `test` parancs alapvető szintaxisa a következő:

```sh
test [options] [arguments]
```

## Common Options
- `-e`: Ellenőrzi, hogy a megadott fájl létezik-e.
- `-f`: Ellenőrzi, hogy a megadott fájl egy normál fájl-e.
- `-d`: Ellenőrzi, hogy a megadott útvonal egy könyvtár-e.
- `-z`: Ellenőrzi, hogy a megadott sztring üres-e.
- `-eq`: Ellenőrzi, hogy két szám egyenlő-e.
- `-gt`: Ellenőrzi, hogy az első szám nagyobb-e a másodiknál.

## Common Examples
Íme néhány gyakori példa a `test` parancs használatára:

1. Fájl létezésének ellenőrzése:
   ```sh
   test -e myfile.txt && echo "A fájl létezik."
   ```

2. Fájl típusának ellenőrzése:
   ```sh
   test -f myfile.txt && echo "Ez egy normál fájl."
   ```

3. Könyvtár ellenőrzése:
   ```sh
   test -d /home/user/documents && echo "Ez egy könyvtár."
   ```

4. Üres sztring ellenőrzése:
   ```sh
   myvar=""
   test -z "$myvar" && echo "A változó üres."
   ```

5. Számok összehasonlítása:
   ```sh
   a=5
   b=10
   test $a -lt $b && echo "$a kisebb, mint $b."
   ```

## Tips
- Használj `&&` operátort a `test` parancs kimenetének feltételes végrehajtásához.
- A `test` parancs alternatív szintaxisa a `[` és `]` karakterek használata, például: `[ -e myfile.txt ]`.
- Mindig idézd be a változókat, hogy elkerüld a hibákat, különösen, ha azok üresek lehetnek.