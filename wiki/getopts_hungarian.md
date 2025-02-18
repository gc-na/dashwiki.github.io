# [Debian] Debian Almquist Shell (dash) getopts használata: Parancssori argumentumok feldolgozása

## Áttekintés
A `getopts` parancs a parancssori argumentumok feldolgozására szolgál. Segítségével könnyen kezelhetjük a parancssori opciókat és argumentumokat, lehetővé téve a felhasználók számára, hogy rugalmasan és hatékonyan használják a shell scriptjeinket.

## Használat
A `getopts` parancs alapvető szintaxisa a következő:

```sh
getopts [opciók] [argumentumok]
```

## Gyakori opciók
- `-a`: Az opciók listájának megadására szolgál.
- `-b`: Az opciók értékeinek megadására.
- `-c`: A parancs végrehajtásának megszakítására.

## Gyakori példák
1. **Egyszerű opciók kezelése**
   ```sh
   #!/bin/dash
   while getopts "ab:" opt; do
       case $opt in
           a)
               echo "A opció aktiválva van."
               ;;
           b)
               echo "B opció értéke: $OPTARG"
               ;;
           *)
               echo "Érvénytelen opció."
               ;;
       esac
   done
   ```

2. **Több opció kezelése**
   ```sh
   #!/bin/dash
   while getopts "abc:" opt; do
       case $opt in
           a)
               echo "A opció aktiválva van."
               ;;
           b)
               echo "B opció aktiválva van."
               ;;
           c)
               echo "C opció értéke: $OPTARG"
               ;;
           *)
               echo "Érvénytelen opció."
               ;;
       esac
   done
   ```

3. **Alapértelmezett értékek beállítása**
   ```sh
   #!/bin/dash
   value="default"
   while getopts "v:" opt; do
       case $opt in
           v)
               value=$OPTARG
               ;;
           *)
               echo "Érvénytelen opció."
               ;;
       esac
   done
   echo "Az érték: $value"
   ```

## Tippek
- Mindig ellenőrizzük a `getopts` által visszaadott opciókat, hogy elkerüljük az érvénytelen bemeneteket.
- Használjunk világos és érthető opcióneveket, hogy a felhasználók könnyen megértsék a script működését.
- Ne felejtsük el a `OPTIND` változót resetelni, ha több `getopts` hívást végzünk a scriptben.