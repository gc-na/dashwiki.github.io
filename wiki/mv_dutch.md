# [Nederlands] Debian Almquist Shell (dash) mv gebruik: Verplaatsen of hernoemen van bestanden

## Overzicht
De `mv`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om bestanden en mappen te verplaatsen of te hernoemen. Dit is een essentiële tool voor bestandsbeheer in de commandoregelomgeving.

## Gebruik
De basis syntaxis van de `mv`-opdracht is als volgt:

```bash
mv [opties] [bronnen] [doel]
```

## Veelvoorkomende opties
- `-i`: Vraagt om bevestiging voordat een bestaande bestemming wordt overschreven.
- `-u`: Verplaatst alleen bestanden die nieuwer zijn dan de bestaande bestanden in de doelmap.
- `-v`: Geeft gedetailleerde informatie over wat er wordt verplaatst of hernoemd.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mv`-opdracht:

1. **Een bestand verplaatsen naar een andere map:**
   ```bash
   mv bestand.txt /pad/naar/doelmap/
   ```

2. **Een bestand hernoemen:**
   ```bash
   mv oud_bestand.txt nieuw_bestand.txt
   ```

3. **Meerdere bestanden verplaatsen naar een andere map:**
   ```bash
   mv bestand1.txt bestand2.txt /pad/naar/doelmap/
   ```

4. **Een bestand verplaatsen met bevestiging bij overschrijven:**
   ```bash
   mv -i bestand.txt /pad/naar/doelmap/
   ```

5. **Alle .txt-bestanden verplaatsen naar een andere map:**
   ```bash
   mv *.txt /pad/naar/doelmap/
   ```

## Tips
- Gebruik de `-i` optie om onbedoeld overschrijven van bestanden te voorkomen.
- Controleer altijd de doelmap voordat je bestanden verplaatst om te zorgen dat je ze niet per ongeluk verliest.
- Maak gebruik van de `-v` optie om te zien wat er precies gebeurt tijdens het verplaatsen of hernoemen van bestanden.