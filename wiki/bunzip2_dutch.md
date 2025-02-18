# [Nederlands] Debian Almquist Shell (dash) bunzip2 gebruik: Bestanden decomprimeren

## Overzicht
De `bunzip2` opdracht wordt gebruikt om bestanden die zijn gecomprimeerd met het bzip2-algoritme te decomprimeren. Het herstelt de originele bestanden uit de gecomprimeerde `.bz2`-bestanden.

## Gebruik
De basis syntaxis van de `bunzip2` opdracht is als volgt:

```bash
bunzip2 [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-k` : Houd het originele gecomprimeerde bestand (`.bz2`) na decompressie.
- `-f` : Forceer decomprimeren, zelfs als het doelbestand al bestaat.
- `-v` : Toon gedetailleerde informatie tijdens het decomprimeren.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `bunzip2`:

1. Een enkel `.bz2`-bestand decomprimeren:
   ```bash
   bunzip2 bestand.bz2
   ```

2. Een bestand decomprimeren en het originele bestand behouden:
   ```bash
   bunzip2 -k bestand.bz2
   ```

3. Een bestand decomprimeren met geforceerde optie:
   ```bash
   bunzip2 -f bestand.bz2
   ```

4. Decompressie met gedetailleerde uitvoer:
   ```bash
   bunzip2 -v bestand.bz2
   ```

## Tips
- Gebruik de `-k` optie als je het originele bestand wilt behouden voor toekomstig gebruik.
- Controleer altijd of er voldoende schijfruimte beschikbaar is voordat je grote bestanden decomprimeert.
- Combineer `bunzip2` met andere commando's zoals `tar` voor het decompressieproces van archieven die meerdere bestanden bevatten.