# [Nederlands] Debian Almquist Shell (dash) trap gebruik: Beheer signalen en exit-statussen

## Overzicht
De `trap`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om signalen en exit-statussen te beheren. Het stelt gebruikers in staat om specifieke acties uit te voeren wanneer een script een bepaald signaal ontvangt of wanneer het normaal of abnormaal eindigt.

## Gebruik
De basis syntaxis van de `trap`-opdracht is als volgt:

```sh
trap [opties] [commando's]
```

## Veelvoorkomende Opties
- `SIGINT`: Dit signaal wordt verzonden wanneer de gebruiker Ctrl+C indrukt. Je kunt een commando specificeren dat moet worden uitgevoerd wanneer dit signaal wordt ontvangen.
- `EXIT`: Dit signaal wordt verzonden wanneer het script normaal eindigt. Hiermee kun je opruimacties uitvoeren.
- `SIGTERM`: Dit signaal wordt gebruikt om een proces te beëindigen. Je kunt een actie definiëren voor wanneer dit signaal wordt ontvangen.

## Veelvoorkomende Voorbeelden

1. **Een eenvoudige trap voor SIGINT:**
   Dit voorbeeld toont hoe je een bericht kunt weergeven wanneer het script wordt onderbroken met Ctrl+C.

   ```sh
   trap 'echo "Script onderbroken!"' SIGINT
   while true; do
       echo "Voer iets in (Ctrl+C om te stoppen)"
       sleep 1
   done
   ```

2. **Opruimen bij het beëindigen van een script:**
   Dit voorbeeld laat zien hoe je een opruimactie kunt uitvoeren wanneer het script normaal eindigt.

   ```sh
   trap 'echo "Opruimen..."; rm -f temp.txt' EXIT
   touch temp.txt
   echo "Dit is een tijdelijke bestand."
   ```

3. **Afhandelen van SIGTERM:**
   In dit voorbeeld wordt een bericht weergegeven wanneer het script een SIGTERM-signaal ontvangt.

   ```sh
   trap 'echo "Ontvangen SIGTERM, beëindigen..."' SIGTERM
   while true; do
       sleep 1
   done
   ```

## Tips
- Gebruik `trap` om ervoor te zorgen dat je scripts netjes worden afgesloten, zelfs als ze worden onderbroken.
- Test je scripts grondig om te zien hoe ze zich gedragen bij verschillende signalen.
- Vergeet niet dat je meerdere signalen kunt afhandelen met één `trap`-opdracht door ze te scheiden met spaties.