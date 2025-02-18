# [Nederlands] Debian Almquist Shell (dash) traceroute gebruik: Netwerkpaden traceren

## Overzicht
De `traceroute`-opdracht is een netwerkdiagnosetool die de route toont die pakketten volgen van de bron naar een opgegeven bestemming. Het geeft inzicht in de verschillende knooppunten die de gegevens passeren, evenals de tijd die elk knooppunt nodig heeft om te reageren.

## Gebruik
De basis syntaxis van de `traceroute`-opdracht is als volgt:

```bash
traceroute [opties] [doel]
```

## Veelvoorkomende Opties
- `-m <max_ttl>`: Stel de maximale Time-To-Live (TTL) in voor de pakketten.
- `-n`: Voorkom het omzetten van hostnamen naar IP-adressen, wat de snelheid kan verhogen.
- `-p <poort>`: Specificeer de poort die moet worden gebruikt voor de traceroute.
- `-q <aantal>`: Geef het aantal probe-pakketten op dat naar elke hop moet worden verzonden.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `traceroute`:

1. Basis traceroute naar een website:
   ```bash
   traceroute www.example.com
   ```

2. Traceroute met een maximale TTL van 30:
   ```bash
   traceroute -m 30 www.example.com
   ```

3. Traceroute zonder hostnamen op te lossen:
   ```bash
   traceroute -n www.example.com
   ```

4. Traceroute naar een IP-adres met een specifieke poort:
   ```bash
   traceroute -p 80 192.168.1.1
   ```

5. Traceroute met meerdere probes per hop:
   ```bash
   traceroute -q 5 www.example.com
   ```

## Tips
- Gebruik de `-n` optie als je snelheid wilt verbeteren, vooral bij netwerken met veel DNS-resolutie.
- Controleer de resultaten op ongebruikelijke vertragingen of time-outs, wat kan wijzen op netwerkproblemen.
- Combineer `traceroute` met andere netwerktools zoals `ping` voor een uitgebreidere diagnose van netwerkproblemen.