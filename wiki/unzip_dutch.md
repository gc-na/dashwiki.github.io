# [Nederlands] Debian Almquist Shell (dash) unzip gebruik: Bestanden uitpakken

## Overzicht
De `unzip`-opdracht wordt gebruikt om gecomprimeerde ZIP-bestanden uit te pakken. Het is een handige manier om bestanden te extraheren die zijn opgeslagen in een ZIP-archief.

## Gebruik
De basis syntaxis van de `unzip`-opdracht is als volgt:

```bash
unzip [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`: Lijst de inhoud van het ZIP-bestand zonder het uit te pakken.
- `-d <directory>`: Specificeert de doelmap waar de bestanden moeten worden uitgepakt.
- `-o`: Overschrijft bestaande bestanden zonder bevestiging.
- `-q`: Voert de opdracht uit in stille modus, zonder uitvoer naar de terminal.

## Veelvoorkomende voorbeelden
1. **Een ZIP-bestand uitpakken naar de huidige map:**
   ```bash
   unzip bestand.zip
   ```

2. **Een ZIP-bestand uitpakken naar een specifieke map:**
   ```bash
   unzip bestand.zip -d /pad/naar/doelmap
   ```

3. **De inhoud van een ZIP-bestand weergeven zonder uit te pakken:**
   ```bash
   unzip -l bestand.zip
   ```

4. **Een ZIP-bestand uitpakken en bestaande bestanden overschrijven:**
   ```bash
   unzip -o bestand.zip
   ```

## Tips
- Controleer altijd de inhoud van een ZIP-bestand met de `-l` optie voordat je het uitpakt, vooral als je niet zeker weet wat erin zit.
- Gebruik de `-d` optie om bestanden georganiseerd uit te pakken in specifieke mappen.
- Wees voorzichtig met de `-o` optie, omdat deze bestaande bestanden zonder waarschuwing kan overschrijven.