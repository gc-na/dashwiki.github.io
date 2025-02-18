# [Nederlands] Debian Almquist Shell (dash) du: [gebruiksruimte van bestanden en mappen]

## Overzicht
De `du` (disk usage) opdracht wordt gebruikt om de schijfruimte die door bestanden en mappen wordt gebruikt te rapporteren. Het geeft een overzicht van de grootte van bestanden en directories, wat nuttig kan zijn voor het beheren van schijfruimte.

## Gebruik
De basis syntaxis van de `du` opdracht is als volgt:

```
du [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Toont de grootte in een leesbaar formaat (bijv. KB, MB).
- `-s`: Geeft alleen de totale grootte van de opgegeven directory weer.
- `-a`: Toont de grootte van alle bestanden, niet alleen directories.
- `-c`: Geeft een totaal weer van de schijfruimte aan het einde van de uitvoer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `du` opdracht:

1. Toon de schijfruimte van de huidige directory in een leesbaar formaat:
   ```bash
   du -h
   ```

2. Toon alleen de totale grootte van een specifieke directory:
   ```bash
   du -sh /pad/naar/directory
   ```

3. Toon de grootte van alle bestanden en subdirectories in een directory:
   ```bash
   du -ah /pad/naar/directory
   ```

4. Toon de grootte van een directory en geef een totaal weer:
   ```bash
   du -ch /pad/naar/directory
   ```

## Tips
- Gebruik de `-h` optie om de uitvoer gemakkelijker te lezen, vooral als je met grote bestanden werkt.
- Combineer `du` met andere opdrachten zoals `sort` om de grootste bestanden of directories bovenaan te krijgen:
  ```bash
  du -ah /pad/naar/directory | sort -hr | head -n 10
  ```
- Vergeet niet dat `du` ook kan worden uitgevoerd met sudo als je toegang nodig hebt tot bepaalde directories waarvoor je geen rechten hebt.