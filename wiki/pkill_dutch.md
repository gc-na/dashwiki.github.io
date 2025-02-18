# [Nederlands] Debian Almquist Shell (dash) pkill gebruik: Proces beëindigen op basis van naam

## Overzicht
De `pkill`-opdracht wordt gebruikt om processen te beëindigen op basis van hun naam of andere eigenschappen. Dit is handig wanneer je een of meerdere processen wilt afsluiten zonder hun proces-ID's (PID's) te hoeven opzoeken.

## Gebruik
De basis syntaxis van de `pkill`-opdracht is als volgt:

```bash
pkill [opties] [argumenten]
```

## Veelvoorkomende opties
- `-f`: Zoek naar de volledige opdrachtregel in plaats van alleen de procesnaam.
- `-n`: Beëindig alleen de nieuwste instantie van het proces.
- `-o`: Beëindig alleen de oudste instantie van het proces.
- `-signal`: Geef het signaal op dat naar de processen moet worden gestuurd (standaard is TERM).

## Veelvoorkomende voorbeelden

1. Beëindig een proces op basis van de naam:
   ```bash
   pkill firefox
   ```

2. Beëindig een proces met een specifiek signaal:
   ```bash
   pkill -9 firefox
   ```

3. Beëindig alleen de nieuwste instantie van een proces:
   ```bash
   pkill -n firefox
   ```

4. Beëindig processen op basis van de volledige opdrachtregel:
   ```bash
   pkill -f 'python script.py'
   ```

5. Beëindig een proces met een specifiek signaal en gebruik een patroon:
   ```bash
   pkill -SIGTERM -f 'java -jar myapp.jar'
   ```

## Tips
- Wees voorzichtig met het gebruik van `pkill`, vooral met krachtige signalen zoals `-9`, omdat dit processen onmiddellijk beëindigt zonder ze de kans te geven om op te schonen.
- Gebruik de `-n` en `-o` opties om meer controle te krijgen over welke processen je beëindigt.
- Test je `pkill`-commando met een onschadelijk signaal (zoals `-0`, dat geen effect heeft) om te zien welke processen getroffen zouden worden, voordat je ze daadwerkelijk beëindigt.