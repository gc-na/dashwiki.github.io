# [Nederlands] Debian Almquist Shell (dash) cmp gebruik: Vergelijk bestanden byte voor byte

## Overzicht
De `cmp`-opdracht wordt gebruikt om twee bestanden byte voor byte te vergelijken. Het geeft de eerste locatie weer waar de bestanden verschillen. Dit is handig voor het controleren van de integriteit van bestanden of het verifiëren van de inhoud.

## Gebruik
De basis syntaxis van de `cmp`-opdracht is als volgt:

```bash
cmp [opties] [bestanden]
```

## Veelvoorkomende Opties
- `-l`: Toon de verschillen in octale waarden.
- `-s`: Stil; geen uitvoer, alleen de exitstatus.
- `-i OFFSET`: Begin de vergelijking bij de opgegeven offset.
- `-n N`: Vergelijk slechts de eerste N bytes van de bestanden.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cmp`-opdracht:

1. Vergelijk twee bestanden en toon de eerste verschillen:
   ```bash
   cmp bestand1.txt bestand2.txt
   ```

2. Vergelijk bestanden zonder uitvoer, alleen de exitstatus:
   ```bash
   cmp -s bestand1.txt bestand2.txt
   ```

3. Vergelijk de eerste 100 bytes van twee bestanden:
   ```bash
   cmp -n 100 bestand1.txt bestand2.txt
   ```

4. Toon de verschillen in octale waarden:
   ```bash
   cmp -l bestand1.txt bestand2.txt
   ```

## Tips
- Gebruik de `-s` optie als je alleen wilt weten of de bestanden verschillen zonder verdere uitvoer.
- Combineer `cmp` met andere commando's zoals `grep` om specifieke verschillen te filteren.
- Vergeet niet dat `cmp` alleen werkt met reguliere bestanden en niet met directories of speciale bestanden.