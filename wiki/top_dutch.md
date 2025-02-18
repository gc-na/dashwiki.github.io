# [Nederlands] Debian Almquist Shell (dash) top gebruik: Toont systeemprocessen in real-time

## Overzicht
De `top`-opdracht is een krachtige tool die in real-time informatie geeft over de actieve processen op een systeem. Het toont een dynamische weergave van de systeemstatus, inclusief CPU- en geheugengebruik, waardoor gebruikers eenvoudig kunnen zien welke processen veel middelen verbruiken.

## Gebruik
De basis syntaxis van de `top`-opdracht is als volgt:

```bash
top [opties]
```

## Veelvoorkomende opties
- `-d <tijd>`: Stel de update-intervaltijd in (in seconden).
- `-n <aantal>`: Geef het aantal updates op dat moet worden weergegeven voordat `top` stopt.
- `-b`: Voer `top` uit in batch-modus, wat handig is voor scripting.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `top`-opdracht:

1. **Start top met de standaardinstellingen**:
   ```bash
   top
   ```

2. **Stel het update-interval in op 2 seconden**:
   ```bash
   top -d 2
   ```

3. **Voer top uit in batch-modus en sla de output op in een bestand**:
   ```bash
   top -b -n 5 > top_output.txt
   ```

4. **Bekijk alleen processen van een specifieke gebruiker**:
   ```bash
   top -u gebruikersnaam
   ```

## Tips
- Gebruik de toetsen `h` of `?` binnen `top` voor een helpmenu met sneltoetsen.
- Druk op `k` om een proces te beëindigen door het PID in te voeren.
- Gebruik `Shift + M` om processen te sorteren op geheugengebruik en `Shift + P` voor CPU-gebruik.