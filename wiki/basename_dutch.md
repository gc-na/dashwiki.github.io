# [Nederlands] Debian Almquist Shell (dash) basename gebruik: [verwijder bestandspaden]

## Overzicht
De `basename` opdracht in de Debian Almquist Shell (dash) wordt gebruikt om het laatste deel van een pad naar een bestand of een directory te extraheren. Dit is handig wanneer je alleen de bestandsnaam wilt zonder het volledige pad.

## Gebruik
De basis syntaxis van de `basename` opdracht is als volgt:

```bash
basename [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`: Verwerkt meerdere argumenten en geeft de basenames van elk bestand terug.
- `-s`: Verwijdert een specifieke suffix van de bestandsnaam.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Basisgebruik
Om de naam van een bestand uit een pad te halen:

```bash
basename /usr/local/bin/script.sh
```
**Uitvoer:** `script.sh`

### Voorbeeld 2: Meerdere bestandsnamen
Om de basenames van meerdere bestanden te verkrijgen:

```bash
basename -a /usr/local/bin/script.sh /usr/bin/another_script.py
```
**Uitvoer:**
```
script.sh
another_script.py
```

### Voorbeeld 3: Suffix verwijderen
Om een suffix van een bestandsnaam te verwijderen:

```bash
basename -s .sh /usr/local/bin/script.sh
```
**Uitvoer:** `script`

## Tips
- Gebruik `basename` in scripts om bestandsnamen dynamisch te extraheren zonder het pad.
- Combineer `basename` met andere commando's zoals `find` om efficiënter met bestanden te werken.
- Wees voorzichtig met het gebruik van de `-s` optie; zorg ervoor dat de suffix die je opgeeft daadwerkelijk in de bestandsnaam voorkomt om verwarring te voorkomen.