# [Nederlands] Debian Almquist Shell (dash) true gebruik: Altijd succesvol beëindigen

## Overzicht
De `true` opdracht in de Debian Almquist Shell (dash) is een eenvoudige opdracht die altijd met een succesvolle statuscode (0) eindigt. Het wordt vaak gebruikt in scripts om aan te geven dat een bepaalde actie succesvol is uitgevoerd, of om een lege plaats in te vullen waar een opdracht vereist is.

## Gebruik
De basis syntaxis van de `true` opdracht is als volgt:

```sh
true [opties] [argumenten]
```

## Veelvoorkomende opties
De `true` opdracht heeft geen specifieke opties of argumenten, omdat het altijd succesvol eindigt zonder enige uitvoering of output.

## Veelvoorkomende Voorbeelden

Hier zijn enkele praktische voorbeelden van het gebruik van de `true` opdracht:

### Voorbeeld 1: Gebruik in een script
```sh
#!/bin/dash
# Dit script doet niets en eindigt altijd succesvol
true
echo "Het script is succesvol uitgevoerd."
```

### Voorbeeld 2: In een while-lus
```sh
while true; do
    echo "Dit blijft doorgaan totdat je het script stopt."
    sleep 1
done
```

### Voorbeeld 3: Voorwaardelijke uitvoering
```sh
if true; then
    echo "Deze boodschap wordt altijd weergegeven."
fi
```

## Tips
- Gebruik `true` in scripts om een placeholder te creëren waar een opdracht vereist is, maar je geen actie wilt uitvoeren.
- Het kan nuttig zijn in combinatie met andere opdrachten zoals `&&` en `||` om de flow van een script te beheren.
- Aangezien `true` geen output genereert, is het handig voor het minimaliseren van onnodige uitvoer in scripts.