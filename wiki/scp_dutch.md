# [Nederlands] Debian Almquist Shell (dash) scp gebruik: Bestanden veilig kopiëren

## Overzicht
Het `scp` (secure copy) commando wordt gebruikt om bestanden veilig over een netwerk te kopiëren. Het maakt gebruik van SSH (Secure Shell) om gegevens te versleutelen tijdens de overdracht, waardoor het een veilige manier is om bestanden tussen lokale en externe systemen te verplaatsen.

## Gebruik
De basis syntaxis van het `scp` commando is als volgt:

```bash
scp [opties] [bron] [doel]
```

## Veelvoorkomende Opties
- `-r`: Kopieert directories recursief.
- `-P`: Specificeert de poort die gebruikt moet worden voor SSH (let op de hoofdletter).
- `-i`: Geeft een specifieke SSH-sleutel op voor authenticatie.
- `-v`: Geeft gedetailleerde uitvoer voor debugging.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `scp`:

1. **Kopieer een lokaal bestand naar een externe server:**
   ```bash
   scp /pad/naar/lokaal_bestand.txt gebruiker@server:/pad/naar/doel/
   ```

2. **Kopieer een bestand van een externe server naar de lokale machine:**
   ```bash
   scp gebruiker@server:/pad/naar/externe_bestand.txt /pad/naar/lokaal/
   ```

3. **Kopieer een hele directory naar een externe server:**
   ```bash
   scp -r /pad/naar/lokale_directory gebruiker@server:/pad/naar/doel/
   ```

4. **Kopieer een bestand met een specifieke SSH-poort:**
   ```bash
   scp -P 2222 /pad/naar/lokaal_bestand.txt gebruiker@server:/pad/naar/doel/
   ```

## Tips
- Zorg ervoor dat je de juiste rechten hebt op de doelmachine om bestanden te kunnen kopiëren.
- Gebruik de `-v` optie voor gedetailleerde uitvoer als je problemen ondervindt bij het kopiëren.
- Overweeg het gebruik van SSH-sleutels voor een veiligere en eenvoudigere authenticatie.