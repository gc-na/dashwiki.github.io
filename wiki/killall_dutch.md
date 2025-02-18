# [Nederlands] Debian Almquist Shell (dash) killall gebruik: Beëindig processen op basis van naam

## Overzicht
De `killall` opdracht in de Debian Almquist Shell (dash) wordt gebruikt om alle processen met een bepaalde naam te beëindigen. Dit is handig wanneer je meerdere instanties van een programma wilt afsluiten zonder ze één voor één te hoeven zoeken.

## Gebruik
De basis syntaxis van de `killall` opdracht is als volgt:

```bash
killall [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-u <gebruiker>`: Beëindig alleen processen die door de opgegeven gebruiker zijn gestart.
- `-i`: Vraag bevestiging voordat een proces wordt beëindigd.
- `-q`: Stilte modus; geen foutmeldingen tonen als er geen processen worden gevonden.
- `-s <signaal>`: Geef een specifiek signaal door om naar de processen te sturen (standaard is SIGTERM).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `killall`:

1. Beëindig alle processen met de naam `firefox`:
   ```bash
   killall firefox
   ```

2. Beëindig alle processen met de naam `python`, maar vraag om bevestiging:
   ```bash
   killall -i python
   ```

3. Beëindig alle processen die door de gebruiker `jan` zijn gestart:
   ```bash
   killall -u jan
   ```

4. Stuur een SIGKILL signaal naar alle processen met de naam `gedit`:
   ```bash
   killall -s SIGKILL gedit
   ```

5. Gebruik de stille modus om processen te beëindigen zonder foutmeldingen:
   ```bash
   killall -q vlc
   ```

## Tips
- Wees voorzichtig met het gebruik van `killall`, vooral met krachtige signalen zoals SIGKILL, omdat dit kan leiden tot dataverlies.
- Controleer altijd welke processen je wilt beëindigen met `ps` of `pgrep` voordat je `killall` gebruikt.
- Gebruik de `-i` optie als je twijfelt, zodat je bevestiging krijgt voordat processen worden beëindigd.