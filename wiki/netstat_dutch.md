# [Nederlands] Debian Almquist Shell (dash) netstat gebruik: Netwerkverbindingen en statistieken bekijken

## Overzicht
Het `netstat` commando is een krachtig hulpmiddel dat informatie biedt over netwerkverbindingen, routingtabellen, interface-statistieken en meer. Het helpt gebruikers om inzicht te krijgen in actieve verbindingen en netwerkactiviteit op hun systeem.

## Gebruik
De basis syntaxis van het `netstat` commando is als volgt:

```bash
netstat [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelgebruikte opties voor `netstat`:

- `-a`: Toont alle verbindingen en luisterende poorten.
- `-t`: Toont alleen TCP-verbindingen.
- `-u`: Toont alleen UDP-verbindingen.
- `-n`: Toont IP-adressen en poorten in plaats van hostnamen.
- `-l`: Toont alleen de poorten die aan het luisteren zijn.
- `-p`: Toont het proces dat de verbinding gebruikt.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `netstat`:

1. **Alle actieve verbindingen weergeven:**
   ```bash
   netstat -a
   ```

2. **Alle TCP-verbindingen weergeven:**
   ```bash
   netstat -t
   ```

3. **Alle UDP-verbindingen weergeven:**
   ```bash
   netstat -u
   ```

4. **Actieve verbindingen met procesinformatie:**
   ```bash
   netstat -p
   ```

5. **Luisterende poorten weergeven:**
   ```bash
   netstat -l
   ```

6. **Verbindingen weergeven met IP-adressen in plaats van hostnamen:**
   ```bash
   netstat -n
   ```

## Tips
- Gebruik de optie `-n` om de uitvoer te versnellen, vooral als je veel verbindingen hebt.
- Combineer opties voor meer gedetailleerde informatie, bijvoorbeeld `netstat -tuln` om zowel TCP als UDP luisterende poorten te tonen met IP-adressen.
- Controleer regelmatig je netwerkverbindingen om ongewenste of verdachte activiteit te identificeren.