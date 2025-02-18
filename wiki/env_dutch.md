# [Nederlands] Debian Almquist Shell (dash) env gebruik: Omgevingsvariabelen beheren

## Overzicht
De `env`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om omgevingsvariabelen te beheren en om programma's uit te voeren met een aangepaste omgeving. Het stelt gebruikers in staat om de omgeving waarin een commando wordt uitgevoerd te configureren, wat handig kan zijn voor het testen of het uitvoeren van scripts met specifieke instellingen.

## Gebruik
De basis syntaxis van de `env`-opdracht is als volgt:

```sh
env [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i`: Start een nieuwe omgeving zonder bestaande omgevingsvariabelen.
- `-u VAR`: Verwijdert de opgegeven omgevingsvariabele `VAR` uit de omgeving.
- `VAR=value`: Stelt een omgevingsvariabele in voor de uitvoering van het volgende commando.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `env`-opdracht:

1. **Weergeven van alle omgevingsvariabelen**:
   ```sh
   env
   ```

2. **Een omgevingsvariabele instellen en een commando uitvoeren**:
   ```sh
   env MY_VAR=Hello world
   ```

3. **Een omgevingsvariabele verwijderen**:
   ```sh
   env -u MY_VAR command
   ```

4. **Een nieuwe omgeving starten zonder bestaande variabelen**:
   ```sh
   env -i bash
   ```

5. **Meerdere omgevingsvariabelen instellen**:
   ```sh
   env VAR1=value1 VAR2=value2 command
   ```

## Tips
- Gebruik `env` om tijdelijke omgevingsvariabelen in scripts te testen zonder de huidige omgeving te beïnvloeden.
- Het gebruik van `-i` is handig voor het debuggen van scripts, omdat het alle bestaande variabelen negeert.
- Vergeet niet dat omgevingsvariabelen hoofdlettergevoelig zijn; `VAR` en `var` worden als verschillende variabelen beschouwd.