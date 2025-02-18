# [Danish] Debian Almquist Shell (dash) exit brug: Afslutning af et script eller en shell-session

## Oversigt
`exit`-kommandoen bruges til at afslutte et script eller en shell-session i Debian Almquist Shell (dash). Når denne kommando udføres, stopper den den aktuelle proces og returnerer en statuskode til det overordnede miljø.

## Brug
Den grundlæggende syntaks for `exit`-kommandoen er som følger:

```sh
exit [statuskode]
```

## Almindelige muligheder
- `statuskode`: En valgfri parameter, der angiver afslutningsstatus. Hvis ingen statuskode angives, returneres status 0, hvilket indikerer succes.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `exit`-kommandoen:

1. Afslut et script med standardstatus (0):
   ```sh
   exit
   ```

2. Afslut et script med en specifik statuskode (f.eks. 1):
   ```sh
   exit 1
   ```

3. Afslut en interaktiv shell-session:
   ```sh
   exit
   ```

4. Afslut et script betinget baseret på en variabel:
   ```sh
   if [ "$FEJL" -eq 1 ]; then
       exit 1
   fi
   ```

## Tips
- Det er en god praksis at angive en statuskode, når du afslutter et script, så andre programmer kan forstå, om det blev udført korrekt.
- Brug statuskoder fra 0 til 255 for at undgå uventede resultater.
- Når du arbejder med shell-scripts, kan du bruge `exit $?` for at afslutte med den sidste kommando's statuskode.