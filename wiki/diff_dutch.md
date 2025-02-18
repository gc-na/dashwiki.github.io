# [Nederlands] Debian Almquist Shell (dash) diff gebruik: Vergelijk bestanden en mappen

## Overzicht
De `diff`-opdracht wordt gebruikt om de verschillen tussen twee bestanden of mappen te vergelijken. Het toont de regels die verschillen tussen de twee invoerbestanden, wat handig is voor het identificeren van wijzigingen in tekstbestanden.

## Gebruik
De basis syntaxis van de `diff`-opdracht is als volgt:

```bash
diff [opties] [argumenten]
```

## Veelvoorkomende opties
- `-u`: Toon de verschillen in een uniforme indeling.
- `-c`: Toon de verschillen in een context-indeling.
- `-i`: Negeer hoofdlettergevoeligheid bij het vergelijken.
- `-r`: Vergelijk mappen recursief.
- `-q`: Geef alleen aan of de bestanden verschillen, zonder de details te tonen.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basis vergelijking van twee bestanden
```bash
diff bestand1.txt bestand2.txt
```

### Voorbeeld 2: Verschillen in uniforme indeling weergeven
```bash
diff -u bestand1.txt bestand2.txt
```

### Voorbeeld 3: Vergelijk twee mappen recursief
```bash
diff -r map1/ map2/
```

### Voorbeeld 4: Negeer hoofdlettergevoeligheid
```bash
diff -i bestand1.txt bestand2.txt
```

### Voorbeeld 5: Alleen aangeven of bestanden verschillen
```bash
diff -q bestand1.txt bestand2.txt
```

## Tips
- Gebruik de `-u` optie voor een duidelijker overzicht van de verschillen, vooral bij het werken met code.
- Bij het vergelijken van mappen, kan de `-r` optie nuttig zijn om een volledig overzicht van alle verschillen te krijgen.
- Combineer opties zoals `-u` en `-i` voor een meer flexibele vergelijking, afhankelijk van je behoeften.