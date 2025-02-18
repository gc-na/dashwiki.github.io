# [Debian] Debian Almquist Shell (dash) echo használata: Szöveg kiírása a terminálra

## Áttekintés
Az `echo` parancs a Debian Almquist Shell (dash) környezetben a szöveg kiírására szolgál a terminálra. Használható egyszerű üzenetek, változók értékeinek megjelenítésére, vagy akár formázott szöveg kiírására is.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
echo [opciók] [argumentumok]
```

## Gyakori Opciók
- `-n`: Ne írja ki az új sort a végén.
- `-e`: Engedélyezi az escape karakterek értelmezését, mint például `\n` (új sor) vagy `\t` (tabulátor).
- `-E`: Az escape karakterek letiltása (ez az alapértelmezett viselkedés).

## Gyakori Példák
1. Egyszerű szöveg kiírása:
   ```bash
   echo "Helló, világ!"
   ```

2. Változó értékének kiírása:
   ```bash
   név="János"
   echo "Üdvözöllek, $név!"
   ```

3. Új sor nélküli kiírás:
   ```bash
   echo -n "Ez egy sor, "
   echo "ez pedig a folytatás."
   ```

4. Escape karakterek használata:
   ```bash
   echo -e "Első sor\nMásodik sor"
   ```

5. Szöveg kiírása tabulátorral:
   ```bash
   echo -e "Első oszlop\tMásodik oszlop"
   ```

## Tippek
- Használj `-n` opciót, ha nem szeretnéd, hogy az `echo` új sort írjon a végére.
- Az `-e` opcióval lehetőséged van escape karakterek használatára, ami hasznos lehet a formázott szövegek kiírásakor.
- Figyelj arra, hogy a változók kiírásakor a `$` jelet használd, hogy a shell tudja, hogy változót akarsz kiírni.