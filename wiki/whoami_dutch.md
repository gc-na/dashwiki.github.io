# [Nederlands] Debian Almquist Shell (dash) whoami gebruik: Toon de huidige gebruikersnaam

## Overzicht
De `whoami`-opdracht in de Debian Almquist Shell (dash) toont de gebruikersnaam van de huidige gebruiker die is ingelogd op het systeem. Dit is handig om snel te controleren onder welke identiteit je werkt, vooral in omgevingen met meerdere gebruikers of wanneer je verschillende gebruikersaccounts beheert.

## Gebruik
De basis syntaxis van de `whoami`-opdracht is als volgt:

```bash
whoami [opties] [argumenten]
```

## Veelvoorkomende opties
De `whoami`-opdracht heeft geen complexe opties, maar hier zijn enkele nuttige:

- `--help`: Toont een korte helptekst met informatie over het gebruik van de opdracht.
- `--version`: Toont de versie-informatie van de `whoami`-opdracht.

## Veelvoorkomende voorbeelden

Hier zijn enkele praktische voorbeelden van het gebruik van de `whoami`-opdracht:

1. **Toon de huidige gebruikersnaam:**

   ```bash
   whoami
   ```

2. **Toon de helpinformatie:**

   ```bash
   whoami --help
   ```

3. **Toon de versie-informatie:**

   ```bash
   whoami --version
   ```

## Tips
- Gebruik `whoami` in scripts om te controleren of een script wordt uitgevoerd onder de juiste gebruikersaccount.
- Combineer `whoami` met andere opdrachten zoals `echo` om de gebruikersnaam in een boodschap te verwerken, bijvoorbeeld:

   ```bash
   echo "Je bent ingelogd als: $(whoami)"
   ```
- Vergeet niet dat `whoami` alleen de naam van de huidige gebruiker toont en geen andere informatie over het systeem of de gebruikerssessie.