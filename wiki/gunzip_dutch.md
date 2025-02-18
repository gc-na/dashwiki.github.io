# [Nederlands] Debian Almquist Shell (dash) gunzip gebruik: Bestanden decomprimeren

## Overzicht
Het `gunzip`-commando wordt gebruikt om bestanden die zijn gecomprimeerd met het gzip-formaat te decomprimeren. Het herstelt de originele bestanden door de compressie ongedaan te maken, waardoor ze weer toegankelijk zijn in hun oorspronkelijke formaat.

## Gebruik
De basis syntaxis van het `gunzip`-commando is als volgt:

```bash
gunzip [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Schrijf de uitgepakte inhoud naar standaarduitvoer in plaats van naar een bestand.
- `-f`: Forceer decomprimeren, zelfs als het doelbestand al bestaat.
- `-k`: Houd het originele gecomprimeerde bestand na decomprimeren.
- `-v`: Toon gedetailleerde informatie over het decompressieproces.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `gunzip`:

1. Een enkel bestand decomprimeren:
   ```bash
   gunzip bestand.gz
   ```

2. Meerdere bestanden decomprimeren:
   ```bash
   gunzip bestand1.gz bestand2.gz
   ```

3. Decompressie naar standaarduitvoer:
   ```bash
   gunzip -c bestand.gz > uitvoer.txt
   ```

4. Decompressie met behoud van het originele bestand:
   ```bash
   gunzip -k bestand.gz
   ```

5. Gedetailleerde uitvoer van het decompressieproces:
   ```bash
   gunzip -v bestand.gz
   ```

## Tips
- Gebruik de `-k` optie als je het originele gecomprimeerde bestand wilt behouden voor toekomstig gebruik.
- Controleer altijd of er voldoende schijfruimte is voordat je bestanden decomprimeert, omdat de originele bestanden weer worden aangemaakt.
- Als je met meerdere bestanden werkt, kan het handig zijn om een wildcard te gebruiken, zoals `*.gz`, om alle gz-bestanden in een map in één keer te decomprimeren:
  ```bash
  gunzip *.gz
  ```