# [Nederlands] Debian Almquist Shell (dash) printf gebruik: Formatteren van uitvoer

## Overzicht
De `printf`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om geformatteerde uitvoer naar de standaarduitvoer te sturen. Het biedt meer controle over de opmaak van de uitvoer in vergelijking met de eenvoudige `echo`-opdracht.

## Gebruik
De basis syntaxis van de `printf`-opdracht is als volgt:

```sh
printf [opties] FORMAT [argumenten...]
```

## Veelvoorkomende opties
- `-v VAR`: Slaat de uitvoer op in de variabele VAR in plaats van deze naar de standaarduitvoer te sturen.
- `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `--version`: Toont de versie-informatie van de `printf`-opdracht.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Eenvoudige tekstuitvoer
```sh
printf "Hallo, wereld!\n"
```
Dit geeft de tekst "Hallo, wereld!" weer, gevolgd door een nieuwe regel.

### Voorbeeld 2: Geformatteerde getallen
```sh
printf "Het getal is: %.2f\n" 3.14159
```
Dit toont "Het getal is: 3.14", waarbij het getal wordt afgerond op twee decimalen.

### Voorbeeld 3: Meerdere argumenten
```sh
printf "Naam: %s, Leeftijd: %d\n" "Jan" 30
```
Dit geeft "Naam: Jan, Leeftijd: 30" weer, waarbij de string en het geheel getal correct worden geformatteerd.

### Voorbeeld 4: Uitvoer naar een variabele
```sh
printf -v resultaat "De som is: %d" $((2 + 3))
echo "$resultaat"
```
Dit slaat de uitvoer op in de variabele `resultaat` en toont "De som is: 5".

## Tips
- Gebruik `%s` voor strings, `%d` voor gehele getallen en `%.nf` voor floating-point getallen met n decimalen.
- Vergeet niet om `\n` toe te voegen aan het einde van je formatstring om een nieuwe regel te creëren.
- `printf` is nuttig voor scripts waar je consistente opmaak nodig hebt, vooral bij het genereren van rapporten of logs.