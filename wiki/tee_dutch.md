# [Nederlands] Debian Almquist Shell (dash) tee gebruik: [schrijf naar standaarduitvoer en bestanden]

## Overzicht
De `tee`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om de uitvoer van een opdracht zowel naar de standaarduitvoer (meestal het scherm) als naar een of meerdere bestanden te schrijven. Dit is handig wanneer je de uitvoer wilt bekijken en tegelijkertijd wilt opslaan.

## Gebruik
De basis syntaxis van de `tee`-opdracht is als volgt:

```bash
tee [opties] [bestanden]
```

## Veelvoorkomende Opties
- `-a`, `--append`: Voeg de uitvoer toe aan het einde van de opgegeven bestanden in plaats van deze te overschrijven.
- `-i`, `--ignore-interrupts`: Negeer onderbrekingen.
- `--help`: Toon een hulpbericht met informatie over het gebruik van de opdracht.
- `--version`: Toon de versie-informatie van de `tee`-opdracht.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `tee`-opdracht:

1. **Schrijf uitvoer naar een bestand en naar het scherm:**
   ```bash
   echo "Hallo, wereld!" | tee output.txt
   ```

2. **Voeg uitvoer toe aan een bestaand bestand:**
   ```bash
   echo "Nieuwe regel" | tee -a output.txt
   ```

3. **Gebruik `tee` in een pijplijn:**
   ```bash
   ls -l | tee bestand_lijst.txt | grep ".txt"
   ```

4. **Schrijf naar meerdere bestanden:**
   ```bash
   echo "Data naar meerdere bestanden" | tee bestand1.txt bestand2.txt
   ```

## Tips
- Gebruik de `-a` optie als je niet wilt dat de bestaande inhoud van een bestand wordt overschreven.
- Combineer `tee` met andere opdrachten in een pijplijn om de uitvoer te filteren of verder te verwerken.
- Controleer altijd de inhoud van de bestanden na gebruik van `tee` om te bevestigen dat de gegevens correct zijn opgeslagen.