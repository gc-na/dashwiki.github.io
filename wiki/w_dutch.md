# [Nederlands] Debian Almquist Shell (dash) w gebruik: toon ingelogde gebruikers en hun activiteiten

## Overzicht
De `w`-opdracht toont informatie over de momenteel ingelogde gebruikers op het systeem, evenals hun activiteiten. Het geeft een overzicht van wie er is ingelogd, hoe lang ze al zijn ingelogd, en welke processen ze uitvoeren.

## Gebruik
De basis syntaxis van de `w`-opdracht is als volgt:

```
w [opties] [argumenten]
```

## Veelvoorkomende opties
- `-h`: Toon geen koptekst.
- `-s`: Toon een kortere versie van de uitvoer.
- `-u`: Toon de gebruikersnaam in plaats van de gebruikers-ID.

## Veelvoorkomende voorbeelden

1. **Basisgebruik**:
   Toont een overzicht van alle ingelogde gebruikers.
   ```bash
   w
   ```

2. **Korte uitvoer**:
   Toont een kortere versie zonder de koptekst.
   ```bash
   w -s
   ```

3. **Zonder koptekst**:
   Toont de informatie zonder de koptekst bovenaan.
   ```bash
   w -h
   ```

4. **Specifieke gebruiker**:
   Toont informatie over een specifieke gebruiker, bijvoorbeeld "jan".
   ```bash
   w jan
   ```

## Tips
- Gebruik `w` regelmatig om een snel overzicht te krijgen van wie er op het systeem is ingelogd en wat ze doen.
- Combineer `w` met andere commando's zoals `grep` om specifieke gebruikers of activiteiten te filteren.
- Houd rekening met de privacy van andere gebruikers; gebruik `w` op een respectvolle manier.