# [Nederlands] Debian Almquist Shell (dash) watch gebruik: Voortdurend een commando uitvoeren

## Overzicht
De `watch`-opdracht in de Debian Almquist Shell (dash) stelt gebruikers in staat om een commando op regelmatige tijdstippen uit te voeren en de uitvoer in real-time te bekijken. Dit is bijzonder nuttig voor het monitoren van veranderingen in de uitvoer van een commando, zoals systeemstatistieken of logbestanden.

## Gebruik
De basis syntaxis van de `watch`-opdracht is als volgt:

```bash
watch [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n <seconden>`: Bepaalt de intervalduur in seconden tussen de uitvoeringen van het commando. Standaard is dit 2 seconden.
- `-d`: Markeert de wijzigingen in de uitvoer. Dit maakt het gemakkelijker om te zien wat er is veranderd.
- `-t`: Verbergt de titelbalk, wat de uitvoer overzichtelijker maakt.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `watch`-opdracht:

### Voorbeeld 1: Systeemgebruik controleren
```bash
watch -n 5 free -h
```
Dit commando toont elke 5 seconden het geheugenverbruik van het systeem.

### Voorbeeld 2: Bestanden in een directory monitoren
```bash
watch -d ls -l /pad/naar/directory
```
Dit toont een gedetailleerde lijst van bestanden in een specifieke directory en markeert wijzigingen.

### Voorbeeld 3: Procesmonitoring
```bash
watch -n 1 ps aux
```
Dit commando toont elke seconde de actieve processen op het systeem.

## Tips
- Gebruik de `-d` optie om snel veranderingen in de uitvoer te identificeren.
- Pas de intervalduur aan met de `-n` optie om de frequentie van de updates aan te passen aan je behoeften.
- Combineer `watch` met andere commando's om specifieke systeeminformatie of logbestanden te monitoren.