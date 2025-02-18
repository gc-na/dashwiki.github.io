# [Nederlands] Debian Almquist Shell (dash) getopts gebruik: Verwerken van opties in shell-scripts

## Overzicht
De `getopts`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om opties en argumenten in shell-scripts te verwerken. Het maakt het mogelijk om opties met een vooraf gedefinieerde syntaxis te analyseren, wat het eenvoudiger maakt om gebruikersinvoer te beheren.

## Gebruik
De basis syntaxis van de `getopts`-opdracht is als volgt:

```sh
getopts optstring variable
```

Hierbij is `optstring` een tekenreeks die de opties definieert en `variable` de naam van de variabele waarin de optie wordt opgeslagen.

## Veelvoorkomende opties
- `optstring`: Een tekenreeks die de beschikbare opties definieert. Elk teken vertegenwoordigt een optie. Als een optie een argument vereist, wordt het teken gevolgd door een dubbele punt (`:`).
- `variable`: De naam van de variabele die de huidige optie opslaat.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basisopties verwerken
```sh
#!/bin/dash

while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Optie A geselecteerd"
      ;;
    b)
      echo "Optie B met argument: $OPTARG"
      ;;
    c)
      echo "Optie C geselecteerd"
      ;;
    *)
      echo "Ongeldige optie"
      ;;
  esac
done
```

### Voorbeeld 2: Opties met argumenten
```sh
#!/bin/dash

while getopts "f:" opt; do
  case $opt in
    f)
      echo "Bestand opgegeven: $OPTARG"
      ;;
    *)
      echo "Ongeldige optie"
      ;;
  esac
done
```

### Voorbeeld 3: Meerdere opties tegelijk
```sh
#!/bin/dash

while getopts "abc" opt; do
  case $opt in
    a)
      echo "Optie A geselecteerd"
      ;;
    b)
      echo "Optie B geselecteerd"
      ;;
    c)
      echo "Optie C geselecteerd"
      ;;
    *)
      echo "Ongeldige optie"
      ;;
  esac
done
```

## Tips
- Gebruik een dubbele punt (`:`) in de `optstring` voor opties die een argument vereisen.
- Zorg ervoor dat je de `OPTARG`-variabele gebruikt om toegang te krijgen tot de argumenten van opties.
- Vergeet niet om een standaardoptie of een foutmelding toe te voegen voor ongeldige invoer om de gebruikerservaring te verbeteren.