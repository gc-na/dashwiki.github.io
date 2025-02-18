# [Svenska] Debian Almquist Shell (dash) vid at: Schemalägg kommandon

## Översikt
Kommandot `at` används för att schemalägga kommandon som ska köras vid en specifik tidpunkt i framtiden. Det är ett praktiskt verktyg för att automatisera uppgifter utan att behöva använda en mer komplex schemaläggare som cron.

## Användning
Den grundläggande syntaxen för kommandot `at` är:

```
at [alternativ] [argument]
```

## Vanliga alternativ
- `-f [fil]`: Anger en fil som innehåller kommandon som ska köras.
- `-m`: Skicka ett e-postmeddelande när kommandot har körts, även om det inte genererar någon utdata.
- `-q [kö]`: Anger vilken kö som ska användas för att schemalägga kommandot.
- `-t [tid]`: Anger en specifik tid för när kommandot ska köras.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `at`:

1. Schemalägg ett kommando för att köra om 10 minuter:
   ```bash
   echo "echo 'Hej världen!'" | at now + 10 minutes
   ```

2. Schemalägg ett skript för att köras vid en specifik tid:
   ```bash
   at 14:00
   # Inuti at-prompten, skriv:
   /path/to/script.sh
   ```

3. Använd en fil för att schemalägga flera kommandon:
   ```bash
   at -f /path/to/commands.txt now + 1 hour
   ```

4. Schemalägg ett kommando och skicka ett e-postmeddelande när det körs:
   ```bash
   echo "backup.sh" | at -m now + 1 day
   ```

## Tips
- Kontrollera schemalagda jobb med kommandot `atq` för att se en lista över kommandon som väntar på att köras.
- Ta bort ett schemalagt jobb med `atrm [job_id]`, där `[job_id]` är ID:t för jobbet du vill ta bort.
- Använd `-q` för att hantera olika köer om du har flera jobb med olika prioriteringar.