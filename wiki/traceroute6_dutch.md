# [Nederlands] Debian Almquist Shell (dash) traceroute6 gebruik: Netwerkpaden traceren

## Overzicht
De `traceroute6` opdracht wordt gebruikt om het pad te traceren dat IPv6-pakketten volgen van de lokale machine naar een opgegeven bestemming. Het helpt bij het diagnosticeren van netwerkproblemen door de verschillende knooppunten (routers) te tonen die de gegevens passeren.

## Gebruik
De basis syntaxis van de `traceroute6` opdracht is als volgt:

```bash
traceroute6 [opties] [doel]
```

## Veelvoorkomende Opties
- `-m <max_hops>`: Stel het maximale aantal hops in dat gevolgd moet worden.
- `-p <poort>`: Specificeer de poort die gebruikt moet worden voor de traceroute.
- `-w <timeout>`: Stel de timeout in voor elke echo-verzoek.
- `-q <aantal>`: Geef het aantal echo-verzoeken per hop op.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `traceroute6`:

1. **Basis traceroute naar een IPv6-adres:**
   ```bash
   traceroute6 2001:db8::1
   ```

2. **Traceroute met een maximaal aantal hops van 15:**
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. **Traceroute naar een domeinnaam met een specifieke poort:**
   ```bash
   traceroute6 -p 80 www.example.com
   ```

4. **Traceroute met een aangepaste timeout van 2 seconden:**
   ```bash
   traceroute6 -w 2 2001:db8::1
   ```

## Tips
- Zorg ervoor dat je de juiste netwerkverbinding hebt voordat je `traceroute6` uitvoert, omdat een onjuiste configuratie kan leiden tot foutieve resultaten.
- Gebruik de `-m` optie om het aantal hops te beperken, vooral als je een snelle diagnose wilt uitvoeren.
- Combineer `traceroute6` met andere netwerkdiagnosetools zoals `ping` voor een completer beeld van de netwerkstatus.