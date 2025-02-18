# [Nederlands] Debian Almquist Shell (dash) cd gebruik: Verander van map

## Overzicht
De `cd` (change directory) opdracht in de Debian Almquist Shell (dash) wordt gebruikt om van de ene map naar de andere te navigeren. Het stelt gebruikers in staat om hun huidige werkdirectory te wijzigen, wat essentieel is voor het uitvoeren van andere opdrachten in de juiste context.

## Gebruik
De basis syntaxis van de `cd` opdracht is als volgt:

```sh
cd [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-`: Ga terug naar de vorige map.
- `..`: Ga één niveau omhoog in de directorystructuur.
- `~`: Ga naar de home directory van de gebruiker.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cd` opdracht:

1. Ga naar de home directory:
    ```sh
    cd ~
    ```

2. Ga naar een specifieke map, bijvoorbeeld `Documenten`:
    ```sh
    cd ~/Documenten
    ```

3. Ga één niveau omhoog in de directorystructuur:
    ```sh
    cd ..
    ```

4. Ga terug naar de vorige map:
    ```sh
    cd -
    ```

5. Ga naar een map met een relatieve pad:
    ```sh
    cd ../AndereMap
    ```

## Tips
- Gebruik `cd -` om snel terug te schakelen naar de vorige map.
- Combineer `cd` met tab-completion om snel naar mappen te navigeren zonder de volledige naam te typen.
- Controleer altijd je huidige directory met de `pwd` (print working directory) opdracht na het gebruik van `cd` om te bevestigen dat je op de juiste locatie bent.