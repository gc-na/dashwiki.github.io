# [Nederlands] Debian Almquist Shell (dash) tar Gebruik: Archiveren en comprimeren van bestanden

## Overzicht
Het `tar`-commando wordt gebruikt om bestanden en mappen te archiveren. Het kan ook bestanden comprimeren, waardoor het handig is voor back-ups en het verzenden van meerdere bestanden als één enkel bestand.

## Gebruik
De basis syntaxis van het `tar`-commando is als volgt:

```bash
tar [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Maak een nieuw archief.
- `-x`: Extraheer bestanden uit een archief.
- `-f`: Geef de naam van het archief op.
- `-v`: Toon de voortgang van het archiveren of extraheren.
- `-z`: Comprimeer of decomprimeer met gzip.
- `-j`: Comprimeer of decomprimeer met bzip2.

## Veelvoorkomende Voorbeelden

1. **Een archief maken**:
   Maak een archief genaamd `mijn_bestanden.tar` van de map `mijn_map`.

   ```bash
   tar -cvf mijn_bestanden.tar mijn_map
   ```

2. **Een gecomprimeerd archief maken met gzip**:
   Maak een gecomprimeerd archief genaamd `mijn_bestanden.tar.gz`.

   ```bash
   tar -czvf mijn_bestanden.tar.gz mijn_map
   ```

3. **Bestanden extraheren uit een archief**:
   Extraheer bestanden uit `mijn_bestanden.tar`.

   ```bash
   tar -xvf mijn_bestanden.tar
   ```

4. **Gecomprimeerd archief extraheren**:
   Extraheer bestanden uit `mijn_bestanden.tar.gz`.

   ```bash
   tar -xzvf mijn_bestanden.tar.gz
   ```

5. **Inhoud van een archief bekijken**:
   Bekijk de inhoud van `mijn_bestanden.tar`.

   ```bash
   tar -tvf mijn_bestanden.tar
   ```

## Tips
- Gebruik de optie `-v` om een overzicht te krijgen van de bestanden die worden gearchiveerd of geëxtraheerd.
- Zorg ervoor dat je voldoende schijfruimte hebt bij het maken van archieven, vooral bij het gebruik van compressie.
- Overweeg om een bestandsnaam met een duidelijke extensie te gebruiken, zoals `.tar`, `.tar.gz`, of `.tar.bz2`, om het type archief aan te geven.