# [Nederlands] Debian Almquist Shell (dash) sed Gebruik: tekstverwerking en -manipulatie

## Overzicht
De `sed` (stream editor) opdracht is een krachtige tool voor tekstverwerking in de Debian Almquist Shell (dash). Het stelt gebruikers in staat om tekstbestanden te bewerken, te transformeren en te manipuleren door middel van verschillende bewerkingscommando's.

## Gebruik
De basis syntaxis van de `sed` opdracht is als volgt:

```bash
sed [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-e`: Voegt een bewerkingscommando toe.
- `-i`: Wijzigt het bestand in plaats van de uitvoer naar de standaarduitvoer te sturen.
- `-n`: Onderdrukt de standaarduitvoer; alleen expliciet aangegeven regels worden weergegeven.
- `s/patroon/vervanging/`: Vervangt het opgegeven patroon door de vervangende tekst.

## Veelvoorkomende Voorbeelden

1. **Eenvoudige tekstvervanging**:
   Vervang "oud" door "nieuw" in een bestand.
   ```bash
   sed 's/oud/nieuw/' bestand.txt
   ```

2. **Wijzigingen in het bestand zelf aanbrengen**:
   Vervang "oud" door "nieuw" en sla de wijzigingen op in hetzelfde bestand.
   ```bash
   sed -i 's/oud/nieuw/' bestand.txt
   ```

3. **Regels selecteren met een patroon**:
   Toon alleen de regels die "belangrijk" bevatten.
   ```bash
   sed -n '/belangrijk/p' bestand.txt
   ```

4. **Meerdere vervangingen in één opdracht**:
   Vervang "eerste" door "tweede" en "derde" door "vierde".
   ```bash
   sed -e 's/eerste/tweede/' -e 's/derde/vierde/' bestand.txt
   ```

## Tips
- Gebruik de `-i` optie met voorzichtigheid, vooral bij belangrijke bestanden; maak altijd een back-up voordat je wijzigingen aanbrengt.
- Test je `sed` commando's zonder de `-i` optie om te zien wat de uitvoer zal zijn voordat je het bestand daadwerkelijk wijzigt.
- Combineer `sed` met andere commando's zoals `grep` of `awk` voor geavanceerdere tekstverwerkingstaken.