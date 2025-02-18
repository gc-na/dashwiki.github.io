# [Nederlands] Debian Almquist Shell (dash) shift gebruik: Verplaatsen van positieparameters

## Overzicht
De `shift`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om de positieparameters van een script of een shell-omgeving te verschuiven. Dit betekent dat de argumenten die aan een script zijn doorgegeven, naar links worden verplaatst, waardoor de eerste parameter wordt verwijderd en de rest naar voren schuift.

## Gebruik
De basis syntaxis van de `shift`-opdracht is als volgt:

```sh
shift [n]
```

Hierbij is `n` het aantal posities dat je wilt verschuiven. Als `n` niet wordt opgegeven, wordt standaard 1 gebruikt.

## Veelvoorkomende opties
- `n`: Het aantal posities om te verschuiven. Als dit niet wordt opgegeven, verschuift `shift` standaard één positie.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basisgebruik
Stel dat je een script hebt dat drie argumenten accepteert:

```sh
#!/bin/dash
echo "Eerste parameter: $1"
echo "Tweede parameter: $2"
echo "Derde parameter: $3"

shift

echo "Na shift:"
echo "Eerste parameter: $1"
echo "Tweede parameter: $2"
```

Als je dit script uitvoert met de argumenten `arg1 arg2 arg3`, zal de uitvoer zijn:

```
Eerste parameter: arg1
Tweede parameter: arg2
Derde parameter: arg3
Na shift:
Eerste parameter: arg2
Tweede parameter: arg3
```

### Voorbeeld 2: Verschoven met een specifiek aantal
Je kunt ook meerdere posities tegelijk verschuiven. Hier is een voorbeeld:

```sh
#!/bin/dash
set -- a b c d e
echo "Voor shift: $1 $2 $3 $4 $5"

shift 2

echo "Na shift 2:"
echo "$1 $2 $3 $4"
```

Bij uitvoering krijg je:

```
Voor shift: a b c d e
Na shift 2:
c d e
```

### Voorbeeld 3: Gebruik in een lus
Je kunt `shift` ook gebruiken in een lus om door alle argumenten te itereren:

```sh
#!/bin/dash
while [ "$#" -gt 0 ]; do
    echo "Huidige parameter: $1"
    shift
done
```

Als je dit script uitvoert met de argumenten `one two three`, zal de uitvoer zijn:

```
Huidige parameter: one
Huidige parameter: two
Huidige parameter: three
```

## Tips
- Gebruik `shift` in combinatie met een controle op het aantal argumenten (`$#`) om te voorkomen dat je probeert te verschuiven wanneer er geen argumenten meer zijn.
- Wees voorzichtig met het gebruik van `shift` in scripts die afhankelijk zijn van specifieke argumentposities, omdat dit de logica van je script kan beïnvloeden.
- Documenteer je scripts goed, zodat anderen begrijpen hoe de `shift`-opdracht de argumenten beïnvloedt.