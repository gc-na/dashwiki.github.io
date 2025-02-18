# [Nederlands] Debian Almquist Shell (dash) hostname gebruik: [toon de systeemnaam]

## Overzicht
De `hostname`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om de naam van de computer of het systeem weer te geven of in te stellen. Dit is nuttig voor netwerkconfiguratie en identificatie van systemen binnen een netwerk.

## Gebruik
De basis syntaxis van de `hostname`-opdracht is als volgt:

```bash
hostname [opties] [argumenten]
```

## Veelvoorkomende opties
- `-f`, `--fqdn`: Toon de volledig gekwalificeerde domeinnaam (FQDN).
- `-s`, `--short`: Toon alleen de korte naam van de host.
- `-i`, `--ip-address`: Toon het IP-adres van de host.
- `-V`, `--version`: Toon de versie van de `hostname`-opdracht.

## Veelvoorkomende voorbeelden

1. **Toon de huidige hostnaam:**
   ```bash
   hostname
   ```

2. **Toon de volledig gekwalificeerde domeinnaam:**
   ```bash
   hostname -f
   ```

3. **Toon alleen de korte naam van de host:**
   ```bash
   hostname -s
   ```

4. **Toon het IP-adres van de host:**
   ```bash
   hostname -i
   ```

5. **Stel een nieuwe hostnaam in:**
   ```bash
   sudo hostname nieuwe-naam
   ```

## Tips
- Gebruik `sudo` bij het instellen van een nieuwe hostnaam, omdat dit meestal root-rechten vereist.
- Controleer na het wijzigen van de hostnaam of deze correct is ingesteld door de `hostname`-opdracht opnieuw uit te voeren.
- Vergeet niet dat het wijzigen van de hostnaam mogelijk ook andere configuraties in je systeem kan beïnvloeden, zoals netwerkservices.