# [Nederlands] Debian Almquist Shell (dash) mtr gebruik: Netwerk traceren

## Overzicht
De `mtr` (My Traceroute) opdracht combineert de functionaliteit van `ping` en `traceroute` om netwerkverbindingen te analyseren. Het biedt een dynamische weergave van de route die gegevenspakketten volgen naar een specifieke host, evenals informatie over de latentie en pakketverlies op elk knooppunt.

## Gebruik
De basis syntaxis van de `mtr` opdracht is als volgt:

```
mtr [opties] [doel]
```

## Veelvoorkomende Opties
- `-r`: Voer een rapportmodus uit, wat betekent dat het resultaat in een tekstformaat wordt weergegeven.
- `-c [aantal]`: Stel het aantal pings in dat moet worden verzonden.
- `-i [interval]`: Stel het interval in tussen de pings in seconden.
- `-p`: Voer de opdracht uit in de "ping" modus.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mtr` opdracht:

1. Basis gebruik om de route naar een host te traceren:
   ```bash
   mtr example.com
   ```

2. Rapportmodus gebruiken om een statisch rapport te genereren:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Het aantal pings instellen op 5 met een interval van 1 seconde:
   ```bash
   mtr -c 5 -i 1 example.com
   ```

4. De opdracht in ping-modus uitvoeren:
   ```bash
   mtr -p example.com
   ```

## Tips
- Gebruik de rapportmodus (`-r`) voor een overzichtelijke weergave van de resultaten, vooral als je de output wilt opslaan of delen.
- Experimenteer met verschillende intervallen en aantallen om een beter beeld te krijgen van de netwerkprestaties.
- Houd rekening met firewall-instellingen die mogelijk de resultaten van `mtr` kunnen beïnvloeden, vooral als je geen antwoord krijgt van bepaalde knooppunten.