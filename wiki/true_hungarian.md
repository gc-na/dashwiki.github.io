# [Debian] Debian Almquist Shell (dash) true: mindig sikeres végrehajtás

## Áttekintés
A `true` parancs a Debian Almquist Shell (dash) környezetben egy olyan parancs, amely mindig sikeresen (0-ás kilépési kóddal) tér vissza. Gyakran használják szkriptekben, ahol szükség van egy olyan parancsra, amely nem végez el semmilyen műveletet, de biztosítja a sikeres végrehajtást.

## Használat
A `true` parancs alapvető szintaxisa a következő:

```sh
true [opciók] [argumentumok]
```

## Gyakori opciók
A `true` parancsnak nincsenek specifikus opciói, mivel a funkciója mindig az, hogy sikeresen térjen vissza. Azonban a következő általános opciók léteznek a shell parancsokban:

- `--help`: Megjeleníti a parancs használatára vonatkozó súgót.
- `--version`: Megjeleníti a parancs verzióját.

## Gyakori példák
Íme néhány példa a `true` parancs használatára:

1. **Egyszerű használat:**
   ```sh
   true
   ```

2. **Használat egy if feltételben:**
   ```sh
   if true; then
       echo "Ez mindig sikeres!"
   fi
   ```

3. **Ciklusban való használat:**
   ```sh
   while true; do
       echo "Ez a ciklus folytatódik..."
       sleep 1
   done
   ```

4. **Szkriptekben való alkalmazás:**
   ```sh
   #!/bin/dash
   true
   echo "A szkript sikeresen lefutott."
   ```

## Tippek
- A `true` parancs hasznos lehet szkriptekben, ahol szükség van egy helyettesítő parancsra, amely nem okoz hibát.
- Használhatod a `true` parancsot a hibakezelés egyszerűsítésére, például ha egy parancsot szeretnél elágazás nélkül végrehajtani.
- A `true` parancsot gyakran kombinálják más parancsokkal, hogy biztosítsák a sikeres végrehajtást, például a `&&` operátorral.