# [Nederlands] Debian Almquist Shell (dash) nslookup gebruik: DNS-naamresolutie

## Overzicht
De `nslookup`-opdracht wordt gebruikt om de DNS-naamresolutie uit te voeren. Het stelt gebruikers in staat om de IP-adressen van een domein te vinden of omgekeerd, en biedt informatie over de DNS-server die wordt gebruikt voor de query.

## Gebruik
De basis syntaxis van de `nslookup`-opdracht is als volgt:

```
nslookup [opties] [argumenten]
```

## Veelvoorkomende opties
- `-type=TYPE`: Specificeert het type DNS-record dat moet worden opgezocht (bijvoorbeeld A, MX, TXT).
- `-timeout=SECONDS`: Stelt de tijdslimiet in voor het wachten op een antwoord van de DNS-server.
- `-retry=COUNT`: Bepaalt het aantal pogingen om een DNS-query uit te voeren.

## Veelvoorkomende voorbeelden

1. **Zoek het IP-adres van een domein:**
   ```bash
   nslookup example.com
   ```

2. **Zoek een specifiek type DNS-record (bijvoorbeeld MX-records):**
   ```bash
   nslookup -type=MX example.com
   ```

3. **Gebruik een specifieke DNS-server voor de query:**
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. **Stel een tijdslimiet in voor de query:**
   ```bash
   nslookup -timeout=5 example.com
   ```

## Tips
- Gebruik `nslookup` in combinatie met andere netwerktests om problemen met de netwerkverbinding te diagnosticeren.
- Controleer altijd of je de juiste DNS-server gebruikt, vooral als je problemen ondervindt met naamresolutie.
- Vergeet niet dat `nslookup` een interactief modus heeft; typ gewoon `nslookup` zonder argumenten om in deze modus te komen en voer meerdere queries uit zonder de opdracht opnieuw in te voeren.