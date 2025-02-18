# [Nederlands] Debian Almquist Shell (dash) at: plannen van taken

## Overzicht
De `at`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om taken op een specifieke tijd in de toekomst uit te voeren. Dit is handig voor het automatiseren van taken die op een later tijdstip moeten worden uitgevoerd zonder dat de gebruiker handmatig hoeft in te grijpen.

## Gebruik
De basisstructuur van de `at`-opdracht is als volgt:

```bash
at [opties] [tijd]
```

## Veelvoorkomende Opties
- `-f <bestand>`: Voer de opdrachten uit die in het opgegeven bestand staan.
- `-m`: Stuur een e-mail naar de gebruiker als de taak is uitgevoerd.
- `-q <wachtrij>`: Specificeer de wachtrij waarin de taak moet worden geplaatst.
- `-V`: Geef de versie van `at` weer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `at`-opdracht:

1. **Een eenvoudige taak plannen**
   Plannen om een script uit te voeren om 15:00 uur:
   ```bash
   echo "bash /pad/naar/script.sh" | at 15:00
   ```

2. **Een taak plannen met een specifieke datum**
   Plannen om een bestand te verwijderen op 1 januari om 10:00 uur:
   ```bash
   echo "rm /pad/naar/bestand.txt" | at 10:00 01-01-2024
   ```

3. **Een taak vanuit een bestand uitvoeren**
   Als je meerdere opdrachten in een bestand hebt, kun je deze als volgt uitvoeren:
   ```bash
   at -f /pad/naar/opdrachten.sh 17:00
   ```

4. **Een taak met e-mailnotificatie**
   Plannen om een melding te sturen om 12:00 uur met e-mailnotificatie:
   ```bash
   echo "echo 'Taak uitgevoerd'" | at -m 12:00
   ```

## Tips
- Zorg ervoor dat de tijd die je opgeeft in een correct formaat is (bijvoorbeeld `HH:MM` of `now + 1 hour`).
- Controleer je geplande taken met de `atq`-opdracht om te zien welke taken nog moeten worden uitgevoerd.
- Gebruik `atrm <taak_id>` om een geplande taak te annuleren als dat nodig is.