# [Nederlands] Debian Almquist Shell (dash) df Gebruik: Toont schijfruimte-informatie

## Overzicht
De `df`-opdracht (disk free) toont informatie over de beschikbare en gebruikte schijfruimte op bestandssystemen. Het is een nuttig hulpmiddel om snel inzicht te krijgen in de opslagcapaciteit van je systeem.

## Gebruik
De basis syntaxis van de `df`-opdracht is als volgt:

```bash
df [opties] [argumenten]
```

## Veelvoorkomende opties
- `-h`: Toont de schijfruimte in een leesbaar formaat (bijv. KB, MB, GB).
- `-T`: Toont het type bestandssysteem.
- `-a`: Toont informatie over alle bestandssystemen, inclusief de niet-gebruikte.
- `-i`: Toont informatie over inodes in plaats van schijfruimte.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `df`-opdracht:

1. Toon de schijfruimte in een leesbaar formaat:

    ```bash
    df -h
    ```

2. Toon het type bestandssysteem samen met de schijfruimte:

    ```bash
    df -hT
    ```

3. Toon informatie over alle bestandssystemen:

    ```bash
    df -a
    ```

4. Toon informatie over inodes:

    ```bash
    df -i
    ```

## Tips
- Gebruik de `-h` optie voor een gemakkelijk leesbare uitvoer, vooral als je met grote schijven werkt.
- Combineer opties voor meer gedetailleerde informatie, zoals `df -hT` om zowel de schijfruimte als het bestandssysteemtype te zien.
- Controleer regelmatig de schijfruimte om te voorkomen dat je schijf vol raakt, wat kan leiden tot systeemproblemen.