# [Nederlands] Debian Almquist Shell (dash) rsync gebruik: Bestanden synchroniseren

## Overzicht
De `rsync`-opdracht is een krachtige tool voor het synchroniseren en overdragen van bestanden en mappen tussen verschillende locaties, zowel lokaal als op afstand. Het is efficiënt omdat het alleen de gewijzigde delen van bestanden verzendt, wat tijd en bandbreedte bespaart.

## Gebruik
De basis syntaxis van de `rsync`-opdracht is als volgt:

```bash
rsync [opties] [bronnen] [doel]
```

## Veelvoorkomende Opties
- `-a`: Archiveer modus; kopieert bestanden en mappen recursief en behoudt de meeste eigenschappen.
- `-v`: Verbose; toont gedetailleerde informatie tijdens de overdracht.
- `-z`: Comprimeert de gegevens tijdens de overdracht om bandbreedte te besparen.
- `-r`: Recursief; kopieert mappen en hun inhoud.
- `--delete`: Verwijdert bestanden in de doelmap die niet meer in de bronmap aanwezig zijn.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `rsync`:

1. **Basis synchronisatie van een lokale map naar een andere lokale map:**
   ```bash
   rsync -av /pad/naar/bronnen/ /pad/naar/doel/
   ```

2. **Synchroniseren van een lokale map naar een externe server:**
   ```bash
   rsync -av /pad/naar/bronnen/ gebruiker@server:/pad/naar/doel/
   ```

3. **Synchroniseren met compressie om bandbreedte te besparen:**
   ```bash
   rsync -avz /pad/naar/bronnen/ gebruiker@server:/pad/naar/doel/
   ```

4. **Synchroniseren en verwijderen van bestanden die niet meer bestaan in de bron:**
   ```bash
   rsync -av --delete /pad/naar/bronnen/ gebruiker@server:/pad/naar/doel/
   ```

## Tips
- Gebruik de `-n` of `--dry-run` optie om te zien wat er zou gebeuren zonder daadwerkelijk bestanden te kopiëren of te verwijderen.
- Zorg ervoor dat je altijd een back-up hebt van belangrijke bestanden voordat je de `--delete` optie gebruikt.
- Overweeg om `rsync` te combineren met cron-taken voor automatische back-ups op regelmatige tijdstippen.