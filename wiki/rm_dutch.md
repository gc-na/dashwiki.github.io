# [Nederlands] Debian Almquist Shell (dash) rm gebruik: Verwijder bestanden en mappen

## Overzicht
Het `rm`-commando wordt gebruikt om bestanden en mappen te verwijderen in de Debian Almquist Shell (dash). Het is een krachtig hulpmiddel en moet met voorzichtigheid worden gebruikt, omdat verwijderde bestanden meestal niet kunnen worden hersteld.

## Gebruik
De basis syntaxis van het `rm`-commando is als volgt:

```bash
rm [opties] [argumenten]
```

## Veelvoorkomende opties
- `-f`: Forceert het verwijderen zonder bevestiging, zelfs als bestanden alleen-lezen zijn.
- `-i`: Vraagt om bevestiging voordat elk bestand wordt verwijderd.
- `-r`: Verwijdert mappen en hun inhoud recursief.
- `-v`: Geeft een gedetailleerde uitvoer van wat er wordt verwijderd.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van het `rm`-commando:

1. Een enkel bestand verwijderen:
   ```bash
   rm bestand.txt
   ```

2. Meerdere bestanden tegelijk verwijderen:
   ```bash
   rm bestand1.txt bestand2.txt bestand3.txt
   ```

3. Een map en al zijn inhoud verwijderen:
   ```bash
   rm -r mapnaam
   ```

4. Bevestiging vragen voordat bestanden worden verwijderd:
   ```bash
   rm -i bestand.txt
   ```

5. Dwingt het verwijderen van een bestand zonder bevestiging:
   ```bash
   rm -f bestand.txt
   ```

## Tips
- Gebruik de `-i` optie om per ongeluk verwijderen te voorkomen, vooral bij belangrijke bestanden.
- Controleer altijd de bestanden die je wilt verwijderen met `ls` voordat je het `rm`-commando uitvoert.
- Wees voorzichtig met de `-r` optie, omdat het hele mappen kan verwijderen zonder waarschuwing.