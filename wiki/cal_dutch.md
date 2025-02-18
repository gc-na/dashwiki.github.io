# [Nederlands] Debian Almquist Shell (dash) cal gebruik: Weergave van kalenders

## Overzicht
De `cal`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om kalenders weer te geven. Het biedt een eenvoudige manier om de kalender van een specifieke maand of jaar te bekijken.

## Gebruik
De basis syntaxis van de `cal`-opdracht is als volgt:

```bash
cal [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-m`: Begin de week op maandag in plaats van zondag.
- `-y`: Toon de kalender voor het huidige jaar.
- `-3`: Toon de kalender voor de huidige maand, de vorige maand en de volgende maand.
- `-j`: Toon de kalender met juliaanse datums.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cal`-opdracht:

Toon de kalender voor de huidige maand:
```bash
cal
```

Toon de kalender voor een specifieke maand en jaar (bijvoorbeeld maart 2023):
```bash
cal 03 2023
```

Toon de kalender voor het huidige jaar:
```bash
cal -y
```

Toon de kalender voor de huidige maand, de vorige maand en de volgende maand:
```bash
cal -3
```

Toon de kalender met juliaanse datums:
```bash
cal -j
```

## Tips
- Gebruik de `-m` optie als je wilt dat de week op maandag begint, wat handig kan zijn in sommige landen.
- Combineer opties voor meer specifieke weergaven, zoals `cal -3 -m` om de kalender voor drie maanden met maandag als startdag weer te geven.
- Vergeet niet dat je ook specifieke datums kunt opgeven om de kalender voor die datum te bekijken, wat handig kan zijn voor het plannen van evenementen.