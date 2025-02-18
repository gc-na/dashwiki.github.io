# [Nederlands] Debian Almquist Shell (dash) cp Gebruik: Bestanden kopiëren

## Overzicht
De `cp`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om bestanden en mappen te kopiëren van de ene locatie naar de andere. Het is een essentieel hulpmiddel voor bestandsbeheer in een Unix-achtige omgeving.

## Gebruik
De basis syntaxis van de `cp`-opdracht is als volgt:

```bash
cp [opties] [bronnen] [doel]
```

## Veelvoorkomende Opties
- `-r`: Kopieert mappen en hun inhoud recursief.
- `-i`: Vraagt om bevestiging voordat een bestaand bestand wordt overschreven.
- `-u`: Kopieert alleen als de bron nieuwere bestanden bevat dan de doelbestanden of als de doelbestanden niet bestaan.
- `-v`: Geeft gedetailleerde uitvoer van de bestanden die worden gekopieerd.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cp`-opdracht:

1. Een enkel bestand kopiëren:
   ```bash
   cp bestand.txt /pad/naar/doel/
   ```

2. Een map en zijn inhoud kopiëren:
   ```bash
   cp -r map /pad/naar/doel/
   ```

3. Een bestand kopiëren met bevestiging bij overschrijven:
   ```bash
   cp -i bestand.txt /pad/naar/doel/
   ```

4. Alleen nieuwere bestanden kopiëren:
   ```bash
   cp -u bestand.txt /pad/naar/doel/
   ```

5. Gedetailleerde uitvoer van het kopiëren:
   ```bash
   cp -v bestand.txt /pad/naar/doel/
   ```

## Tips
- Gebruik de `-i` optie om per ongeluk overschrijven van bestanden te voorkomen.
- Voor het kopiëren van grote mappen, gebruik `-r` om ervoor te zorgen dat alle inhoud wordt meegenomen.
- Combineer opties voor meer controle, bijvoorbeeld `cp -riv` om recursief te kopiëren met bevestiging en gedetailleerde uitvoer.