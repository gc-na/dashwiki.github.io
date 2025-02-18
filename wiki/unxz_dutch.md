# [Nederlands] Debian Almquist Shell (dash) unxz gebruik: Bestanden decomprimeren

## Overzicht
De `unxz` opdracht wordt gebruikt om bestanden die zijn gecomprimeerd met het XZ-formaat te decomprimeren. Dit is handig voor het terugbrengen van bestanden naar hun oorspronkelijke formaat, zodat ze kunnen worden gebruikt of bewerkt.

## Gebruik
De basis syntaxis van de `unxz` opdracht is als volgt:

```bash
unxz [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-k`, `--keep`: Houd het originele gecomprimeerde bestand na decompressie.
- `-f`, `--force`: Dwingt decompressie, zelfs als het doelbestand al bestaat.
- `-v`, `--verbose`: Toon gedetailleerde informatie tijdens het decompressieproces.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `unxz` opdracht:

1. Een enkel bestand decomprimeren:
   ```bash
   unxz bestand.xz
   ```

2. Een bestand decomprimeren en het originele bestand behouden:
   ```bash
   unxz -k bestand.xz
   ```

3. Een bestand decomprimeren met gedetailleerde uitvoer:
   ```bash
   unxz -v bestand.xz
   ```

4. Een bestand forceren om te decomprimeren, zelfs als er al een bestand met dezelfde naam bestaat:
   ```bash
   unxz -f bestand.xz
   ```

## Tips
- Zorg ervoor dat je voldoende schijfruimte hebt voordat je een bestand decomprimeert, omdat het originele bestand mogelijk veel ruimte in beslag neemt.
- Gebruik de `-k` optie als je het originele gecomprimeerde bestand wilt behouden voor toekomstig gebruik.
- Controleer altijd de inhoud van het gedecodeerde bestand om er zeker van te zijn dat de decompressie succesvol was.