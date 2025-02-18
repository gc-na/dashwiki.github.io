# [Nederlands] Debian Almquist Shell (dash) grep gebruik: Zoek naar tekst in bestanden

## Overzicht
De `grep`-opdracht is een krachtige tool die wordt gebruikt om tekstpatronen te zoeken binnen bestanden. Het kan helpen bij het filteren van gegevens en het vinden van specifieke informatie in grote hoeveelheden tekst.

## Gebruik
De basis syntaxis van de `grep`-opdracht is als volgt:

```bash
grep [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i`: Negeert hoofdlettergebruik bij het zoeken.
- `-v`: Toont alleen de regels die **niet** overeenkomen met het patroon.
- `-r`: Doorzoekt bestanden in submappen (recursief).
- `-n`: Toont het regelnummer van de overeenkomstige regels.
- `-l`: Toont alleen de namen van bestanden die een overeenkomst bevatten.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `grep`:

1. Zoek naar een specifiek woord in een bestand:
   ```bash
   grep "woord" bestand.txt
   ```

2. Zoek naar een woord zonder hoofdlettergebruik:
   ```bash
   grep -i "woord" bestand.txt
   ```

3. Zoek naar een woord in alle tekstbestanden in de huidige map:
   ```bash
   grep "woord" *.txt
   ```

4. Zoek recursief naar een woord in alle bestanden binnen een map:
   ```bash
   grep -r "woord" /pad/naar/map
   ```

5. Toon de regelnummer van overeenkomsten:
   ```bash
   grep -n "woord" bestand.txt
   ```

## Tips
- Gebruik de optie `-v` om snel te filteren op regels die niet overeenkomen met je zoekopdracht.
- Combineer `grep` met andere opdrachten zoals `ls` of `cat` voor meer geavanceerde zoekopdrachten.
- Maak gebruik van reguliere expressies voor complexere zoekpatronen.