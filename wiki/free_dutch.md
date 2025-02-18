# [Nederlands] Debian Almquist Shell (dash) vrije geheugeninformatie: Toont het geheugenverbruik van het systeem

## Overzicht
De `free`-opdracht in de Debian Almquist Shell (dash) geeft een overzicht van het geheugenverbruik van het systeem. Het toont informatie over het totale geheugen, het gebruikte geheugen, het vrije geheugen en de swapruimte.

## Gebruik
De basis syntaxis van de `free`-opdracht is als volgt:

```bash
free [opties]
```

## Veelvoorkomende opties
- `-h`: Toont de geheugenwaarden in een leesbaar formaat (bijv. KB, MB, GB).
- `-m`: Toont de geheugenwaarden in megabytes.
- `-g`: Toont de geheugenwaarden in gigabytes.
- `-s <tijdsinterval>`: Herhaalt de uitvoer elke `<tijdsinterval>` seconden.
- `-t`: Toont de totale hoeveelheid geheugen, inclusief swap.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `free`-opdracht:

1. Basisinformatie over geheugen:
   ```bash
   free
   ```

2. Geheugeninformatie in een leesbaar formaat:
   ```bash
   free -h
   ```

3. Geheugeninformatie in megabytes:
   ```bash
   free -m
   ```

4. Geheugeninformatie in gigabytes:
   ```bash
   free -g
   ```

5. Geheugeninformatie elke 5 seconden vernieuwen:
   ```bash
   free -s 5
   ```

6. Totale geheugen- en swapinformatie weergeven:
   ```bash
   free -t
   ```

## Tips
- Gebruik de `-h` optie voor een gemakkelijk leesbare uitvoer, vooral als je met grote hoeveelheden geheugen werkt.
- Combineer de `-s` optie met `watch` om continu de geheugenstatus te monitoren:
  ```bash
  watch free -h
  ```
- Controleer regelmatig het geheugenverbruik om te zorgen dat je systeem soepel blijft draaien, vooral op servers of systemen met beperkte middelen.