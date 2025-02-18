# [Nederlands] Debian Almquist Shell (dash) curl gebruik: Haal gegevens van een URL op

## Overzicht
De `curl`-opdracht is een krachtige tool die wordt gebruikt om gegevens van of naar een server te verzenden via verschillende protocollen, waaronder HTTP, HTTPS, FTP en meer. Het is een veelgebruikte opdracht in de commandoregel voor het ophalen van webinhoud, het testen van API's en het downloaden van bestanden.

## Gebruik
De basis syntaxis van de `curl`-opdracht is als volgt:

```bash
curl [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-O`: Download een bestand en behoud de oorspronkelijke bestandsnaam.
- `-L`: Volg omleidingen als de URL wordt omgeleid.
- `-d`: Stuur gegevens als een POST-verzoek.
- `-H`: Voeg een extra HTTP-header toe aan de aanvraag.
- `-u`: Geef gebruikersnaam en wachtwoord op voor basisverificatie.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `curl`:

1. **Een eenvoudige GET-aanroep doen:**
   ```bash
   curl https://www.example.com
   ```

2. **Een bestand downloaden met behoud van de oorspronkelijke naam:**
   ```bash
   curl -O https://www.example.com/bestand.zip
   ```

3. **Volg omleidingen:**
   ```bash
   curl -L https://bit.ly/voorbeeld
   ```

4. **Gegevens verzenden met een POST-verzoek:**
   ```bash
   curl -d "naam=Jan&leeftijd=30" https://www.example.com/api
   ```

5. **Een extra header toevoegen aan de aanvraag:**
   ```bash
   curl -H "Authorization: Bearer jouw_token" https://www.example.com/api
   ```

## Tips
- Gebruik de `-v` optie voor gedetailleerde uitvoer van de aanvraag en het antwoord, wat handig kan zijn voor foutopsporing.
- Combineer `curl` met andere commando's zoals `grep` om specifieke gegevens uit de uitvoer te filteren.
- Sla vaak gebruikte opties op in een alias in je shell-configuratie om tijd te besparen.