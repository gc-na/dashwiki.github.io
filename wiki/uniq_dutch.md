# [Nederlands] Debian Almquist Shell (dash) uniq gebruik: Verwijder dubbele regels

## Overzicht
De `uniq`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om dubbele regels in een tekstbestand te verwijderen. Het houdt alleen de eerste instantie van een reeks gelijke regels en negeert de rest.

## Gebruik
De basis syntaxis van de `uniq`-opdracht is als volgt:

```bash
uniq [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Tel het aantal voorkomens van elke regel.
- `-d`: Toon alleen de regels die meer dan één keer voorkomen.
- `-u`: Toon alleen de unieke regels, die slechts één keer voorkomen.
- `-i`: Negeer hoofdlettergebruik bij het vergelijken van regels.

## Veelvoorkomende Voorbeelden

1. **Basisgebruik**: Verwijder dubbele regels uit een bestand.
   ```bash
   uniq input.txt output.txt
   ```

2. **Tel dubbele regels**: Toon het aantal keren dat elke regel voorkomt.
   ```bash
   uniq -c input.txt
   ```

3. **Toon alleen dubbele regels**: Geef alleen de regels weer die meer dan één keer voorkomen.
   ```bash
   uniq -d input.txt
   ```

4. **Toon alleen unieke regels**: Geef alleen de regels weer die slechts één keer voorkomen.
   ```bash
   uniq -u input.txt
   ```

5. **Hoofdlettergevoeligheid negeren**: Verwijder dubbele regels zonder rekening te houden met hoofdletters.
   ```bash
   uniq -i input.txt output.txt
   ```

## Tips
- Zorg ervoor dat het invoerbestand is gesorteerd voordat je `uniq` gebruikt, omdat het alleen opeenvolgende dubbele regels verwijdert.
- Combineer `uniq` met `sort` voor een efficiënte manier om unieke regels uit een ongeordend bestand te halen:
  ```bash
  sort input.txt | uniq > output.txt
  ```
- Gebruik de `-c` optie om snel een overzicht te krijgen van de frequentie van regels in je bestand.