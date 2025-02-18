# [Nederlands] Debian Almquist Shell (dash) comm: Vergelijk bestanden regel voor regel

## Overzicht
De `comm`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om twee gesorteerde bestanden regel voor regel te vergelijken. Het toont de regels die uniek zijn voor elk bestand en de regels die in beide bestanden voorkomen.

## Gebruik
De basis syntaxis van de `comm`-opdracht is als volgt:

```bash
comm [opties] [bestand1] [bestand2]
```

## Veelvoorkomende Opties
- `-1`: Verberg de regels die alleen in het eerste bestand voorkomen.
- `-2`: Verberg de regels die alleen in het tweede bestand voorkomen.
- `-3`: Verberg de regels die in beide bestanden voorkomen.
- `-i`: Negeer hoofdlettergebruik bij de vergelijking.

## Veelvoorkomende Voorbeelden

1. **Basis vergelijking van twee bestanden**:
   ```bash
   comm bestand1.txt bestand2.txt
   ```

2. **Alleen de regels die in het eerste bestand voorkomen**:
   ```bash
   comm -13 bestand1.txt bestand2.txt
   ```

3. **Alleen de regels die in het tweede bestand voorkomen**:
   ```bash
   comm -12 bestand1.txt bestand2.txt
   ```

4. **Vergelijking zonder hoofdlettergevoeligheid**:
   ```bash
   comm -i bestand1.txt bestand2.txt
   ```

## Tips
- Zorg ervoor dat de bestanden gesorteerd zijn voordat je `comm` gebruikt, anders krijg je mogelijk onverwachte resultaten.
- Je kunt de uitvoer van `comm` combineren met andere opdrachten, zoals `grep`, om specifieke regels te filteren.
- Gebruik de opties om de uitvoer aan te passen aan je behoeften, zodat je alleen de relevante informatie ziet.