# [Nederlands] Debian Almquist Shell (dash) nice gebruik: Beheer van procesprioriteit

## Overzicht
De `nice`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om de prioriteit van een proces te beheren. Hiermee kun je de CPU-tijd die aan een proces wordt toegewezen verhogen of verlagen, wat handig is om systeembronnen efficiënter te gebruiken.

## Gebruik
De basis syntaxis van de `nice`-opdracht is als volgt:

```
nice [opties] [commando] [argumenten]
```

## Veelvoorkomende opties
- `-n`, `--adjustment`: Hiermee kun je de prioriteit van het proces aanpassen. De standaardwaarde is 10, en je kunt waarden van -20 (hoogste prioriteit) tot 19 (laagste prioriteit) gebruiken.
- `-h`, `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `-v`, `--version`: Toont de versie van de `nice`-opdracht.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `nice`:

1. **Een proces starten met een lagere prioriteit:**
   ```bash
   nice -n 10 myscript.sh
   ```

2. **Een proces starten met een hogere prioriteit:**
   ```bash
   nice -n -5 myscript.sh
   ```

3. **De prioriteit van een bestaand proces wijzigen:**
   ```bash
   renice -n 5 -p 1234
   ```

4. **Een achtergrondproces met een specifieke prioriteit starten:**
   ```bash
   nice -n 15 long_running_task &
   ```

## Tips
- Gebruik `nice` voor processen die minder urgent zijn, zodat belangrijke taken meer CPU-tijd kunnen krijgen.
- Controleer de huidige prioriteit van processen met de `ps`-opdracht om te zien waar je `nice` kunt toepassen.
- Wees voorzichtig met het verhogen van de prioriteit van processen, omdat dit de systeemprestaties kan beïnvloeden.