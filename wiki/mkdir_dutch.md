# [Nederlands] Debian Almquist Shell (dash) mkdir gebruik: Maak nieuwe mappen aan

## Overzicht
De `mkdir`-opdracht wordt gebruikt om nieuwe directories (mappen) aan te maken in het bestandssysteem. Dit is een essentiële functie voor het organiseren van bestanden en het structureren van gegevens.

## Gebruik
De basis syntaxis van de `mkdir`-opdracht is als volgt:

```
mkdir [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-p`: Maak ook de ouders van de opgegeven directories aan als ze nog niet bestaan.
- `-m`: Stel de permissies in voor de nieuwe directory.
- `--help`: Toon een korte handleiding over het gebruik van de opdracht.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `mkdir`:

1. Maak een enkele directory aan:
   ```bash
   mkdir nieuwe_map
   ```

2. Maak meerdere directories tegelijk aan:
   ```bash
   mkdir map1 map2 map3
   ```

3. Maak een directory aan met specifieke permissies:
   ```bash
   mkdir -m 755 beveiligde_map
   ```

4. Maak een directory aan met alle bovenliggende directories:
   ```bash
   mkdir -p /pad/naar/nieuwe/directory
   ```

## Tips
- Gebruik de `-p` optie om ervoor te zorgen dat je niet handmatig elke bovenliggende directory hoeft aan te maken.
- Controleer altijd of de directory al bestaat om fouten te voorkomen. Gebruik bijvoorbeeld `mkdir -p` om dit automatisch te doen.
- Denk aan de juiste permissies bij het aanmaken van directories, vooral als je deze met andere gebruikers wilt delen.