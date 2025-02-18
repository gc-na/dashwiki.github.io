# [Danish] Debian Almquist Shell (dash) shift brug: Skift positionsparametre

## Oversigt
`shift`-kommandoen bruges i shell-scripts til at flytte positionsparametrene til venstre. Det betyder, at den første parameter (typisk `$1`) fjernes, og de efterfølgende parametre skubbes en plads til venstre. Dette er nyttigt, når du vil behandle argumenter i en loop eller ændre, hvilke argumenter der er tilgængelige for scriptet.

## Brug
Den grundlæggende syntaks for `shift`-kommandoen er:

```bash
shift [n]
```

Her er `n` antallet af positioner, der skal skiftes. Hvis `n` ikke angives, skiftes der én position.

## Almindelige muligheder
- `n`: Angiver, hvor mange positioner der skal skiftes. Hvis ikke angivet, skiftes der én position.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `shift`:

### Eksempel 1: Grundlæggende brug
```bash
#!/bin/dash
echo "Før shift: $1 $2 $3"
shift
echo "Efter shift: $1 $2 $3"
```
I dette eksempel vil den første parameter blive fjernet, og de efterfølgende parametre vil blive skubbet til venstre.

### Eksempel 2: Skift flere positioner
```bash
#!/bin/dash
echo "Før shift: $1 $2 $3 $4"
shift 2
echo "Efter shift: $1 $2 $3 $4"
```
Her fjernes de to første parametre, og de resterende skubbes til venstre.

### Eksempel 3: Brug i en loop
```bash
#!/bin/dash
while [ "$#" -gt 0 ]; do
    echo "Behandler parameter: $1"
    shift
done
```
I dette eksempel behandles hver parameter én ad gangen, indtil der ikke er flere tilbage.

## Tips
- Brug `shift` i loops for effektivt at håndtere en liste af argumenter.
- Vær opmærksom på, at når du skifter positioner, kan du miste adgang til de skiftede parametre. Overvej at gemme værdierne i variabler, hvis du skal bruge dem senere.
- Test dit script med forskellige antal argumenter for at sikre, at det fungerer korrekt under alle omstændigheder.