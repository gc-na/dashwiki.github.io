# [Nederlands] Debian Almquist Shell (dash) strace gebruik: Volg systeemaanroepen

## Overzicht
De `strace`-opdracht is een krachtig hulpmiddel dat wordt gebruikt om systeemaanroepen en signalen van een proces te volgen. Het biedt inzicht in de interacties tussen een programma en het besturingssysteem, wat handig is voor foutopsporing en prestatie-analyse.

## Gebruik
De basis syntaxis van de `strace`-opdracht is als volgt:

```
strace [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Geeft een samenvatting van de systeemaanroepen en hun tijdsduur.
- `-e trace=<categorie>`: Volgt alleen systeemaanroepen van een specifieke categorie, zoals `file`, `process`, of `network`.
- `-p <pid>`: Volgt een bestaand proces met het opgegeven proces-ID.
- `-o <bestand>`: Schrijft de uitvoer naar een bestand in plaats van naar de standaarduitvoer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `strace`:

1. Volg een nieuw proces:
   ```bash
   strace ls
   ```

2. Volg een bestaand proces met PID 1234:
   ```bash
   strace -p 1234
   ```

3. Volg alleen bestandssystemen aanroepen:
   ```bash
   strace -e trace=file ls
   ```

4. Schrijf de uitvoer naar een bestand:
   ```bash
   strace -o output.txt ls
   ```

5. Krijg een samenvatting van systeemaanroepen:
   ```bash
   strace -c ls
   ```

## Tips
- Gebruik `strace` met `-o` om de uitvoer op te slaan, zodat je deze later kunt analyseren.
- Combineer `strace` met andere hulpprogramma's zoals `grep` om specifieke systeemaanroepen te filteren.
- Wees voorzichtig bij het gebruik van `strace` op productieprocessen, omdat het de prestaties kan beïnvloeden.