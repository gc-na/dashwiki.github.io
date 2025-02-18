# [Debian] Debian Almquist Shell (dash) crontab használata: Ütemezett feladatok kezelése

## Áttekintés
A `crontab` parancs lehetővé teszi ütemezett feladatok automatikus végrehajtását a rendszerben. Ezzel a parancssal különböző időpontokban és időintervallumokban futtathatunk parancsokat vagy szkripteket.

## Használat
A `crontab` parancs alapvető szintaxisa a következő:

```bash
crontab [opciók] [argumentumok]
```

## Gyakori opciók
- `-e`: A felhasználó crontab fájljának szerkesztése.
- `-l`: A felhasználó crontab fájljának megjelenítése.
- `-r`: A felhasználó crontab fájljának törlése.
- `-i`: Megerősítést kér a törlés előtt.

## Gyakori példák
1. **Crontab fájl szerkesztése:**
   ```bash
   crontab -e
   ```
   Ez a parancs megnyitja a felhasználó crontab fájlját egy szerkesztőben, ahol új ütemezett feladatokat adhatunk hozzá vagy módosíthatunk meglévőket.

2. **Crontab fájl megjelenítése:**
   ```bash
   crontab -l
   ```
   Ezzel a paranccsal megtekinthetjük a jelenlegi ütemezett feladatainkat.

3. **Crontab fájl törlése:**
   ```bash
   crontab -r
   ```
   Ez a parancs törli a felhasználó crontab fájlját. Ha a `-i` opciót is használjuk, akkor megerősítést kér a törlés előtt.

4. **Feladat ütemezése minden nap 2:30-kor:**
   ```bash
   30 2 * * * /path/to/script.sh
   ```
   Ez a bejegyzés minden nap 2:30-kor futtatja a megadott szkriptet.

## Tippek
- Mindig teszteljük a szkripteket manuálisan, mielőtt ütemeznénk őket, hogy biztosak legyünk a helyes működésükben.
- Használjunk abszolút elérési utakat a szkriptekhez, hogy elkerüljük a fájlok nem találását.
- Ellenőrizzük a `cron` logokat, ha a feladatok nem futnak le a várt módon, hogy megtudjuk, miért nem sikerültek.