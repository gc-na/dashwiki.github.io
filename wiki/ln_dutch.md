# [Nederlands] Debian Almquist Shell (dash) ln gebruik: Maak harde en symbolische koppelingen

## Overzicht
De `ln`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om koppelingen naar bestanden of mappen te maken. Hiermee kun je zowel harde koppelingen als symbolische koppelingen (symlinks) aanmaken, wat handig is voor het organiseren van bestanden en het besparen van schijfruimte.

## Gebruik
De basis syntaxis van de `ln`-opdracht is als volgt:

```bash
ln [opties] [doel] [koppeling]
```

## Veelvoorkomende Opties
- `-s`: Maak een symbolische koppeling in plaats van een harde koppeling.
- `-f`: Forceer het overschrijven van bestaande koppelingen.
- `-n`: Behandel de doelkoppeling als een normaal bestand, niet als een koppeling.
- `-v`: Toon gedetailleerde uitvoer over wat er gebeurt.

## Veelvoorkomende Voorbeelden

1. **Harde koppeling maken:**
   ```bash
   ln bestand.txt koppeling.txt
   ```
   Dit maakt een harde koppeling genaamd `koppeling.txt` naar `bestand.txt`.

2. **Symbolische koppeling maken:**
   ```bash
   ln -s /pad/naar/bestand.txt koppeling.txt
   ```
   Dit maakt een symbolische koppeling naar `bestand.txt` met de naam `koppeling.txt`.

3. **Bestaande koppeling overschrijven:**
   ```bash
   ln -f bestand2.txt koppeling.txt
   ```
   Dit overschrijft de bestaande `koppeling.txt` met een nieuwe harde koppeling naar `bestand2.txt`.

4. **Symbolische koppeling met gedetailleerde uitvoer:**
   ```bash
   ln -sv /pad/naar/bestand.txt koppeling.txt
   ```
   Dit maakt een symbolische koppeling en toont een bericht over de gemaakte koppeling.

## Tips
- Gebruik symbolische koppelingen voor bestanden die zich op verschillende locaties kunnen bevinden, omdat harde koppelingen alleen binnen dezelfde bestandssysteem kunnen worden gemaakt.
- Controleer altijd of de koppeling correct is gemaakt met de `ls -l` opdracht, die je informatie geeft over de koppeling en het doel.
- Wees voorzichtig met de `-f` optie, omdat deze bestaande bestanden zonder waarschuwing kan overschrijven.