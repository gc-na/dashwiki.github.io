# [Nederlands] Debian Almquist Shell (dash) head gebruik: toon de eerste regels van een bestand

## Overzicht
De `head`-opdracht wordt gebruikt om de eerste regels van een bestand weer te geven. Dit is handig om snel een overzicht te krijgen van de inhoud van een bestand zonder het hele bestand te openen.

## Gebruik
De basis syntaxis van de `head`-opdracht is als volgt:

```bash
head [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n [aantal]`: Geef het opgegeven aantal regels weer. Standaard toont `head` de eerste 10 regels.
- `-c [aantal]`: Geef het opgegeven aantal bytes weer in plaats van regels.
- `-q`: Schakel de weergave van de bestandsnaam uit wanneer meerdere bestanden worden opgegeven.
- `-v`: Toon altijd de bestandsnaam, zelfs als er maar één bestand is.

## Veelvoorkomende Voorbeelden

1. Toon de eerste 10 regels van een bestand:
   ```bash
   head bestand.txt
   ```

2. Toon de eerste 5 regels van een bestand:
   ```bash
   head -n 5 bestand.txt
   ```

3. Toon de eerste 20 bytes van een bestand:
   ```bash
   head -c 20 bestand.txt
   ```

4. Toon de eerste 10 regels van meerdere bestanden:
   ```bash
   head bestand1.txt bestand2.txt
   ```

5. Toon altijd de bestandsnaam bij het weergeven van de inhoud:
   ```bash
   head -v bestand.txt
   ```

## Tips
- Gebruik `head` in combinatie met andere opdrachten, zoals `grep`, om snel de eerste regels van gefilterde resultaten te bekijken.
- Combineer `head` met `less` voor een paginagewijs overzicht van de eerste regels:
  ```bash
  head bestand.txt | less
  ```
- Vergeet niet dat `head` ook kan worden gebruikt met pijpen (`|`) om de uitvoer van andere opdrachten te beperken.