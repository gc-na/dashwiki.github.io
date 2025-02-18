# [Danish] Debian Almquist Shell (dash) wait brug: Vent på baggrundsprocesser

## Oversigt
`wait`-kommandoen bruges i Debian Almquist Shell (dash) til at vente på, at en eller flere baggrundsprocesser afslutter. Det er nyttigt, når du har startet processer i baggrunden og ønsker at sikre, at de er færdige, før du fortsætter med andre opgaver.

## Brug
Den grundlæggende syntaks for `wait`-kommandoen er som følger:

```sh
wait [options] [arguments]
```

## Almindelige muligheder
- `PID`: Angiv den proces-id (PID), du ønsker at vente på. Hvis ingen PID angives, venter `wait` på alle baggrundsprocesser.
- `-n`: Vent på den næste baggrundsproces, der afslutter.

## Almindelige eksempler

1. **Vent på alle baggrundsprocesser:**
   ```sh
   sleep 5 &
   sleep 3 &
   wait
   ```
   I dette eksempel starter vi to `sleep`-kommandoer i baggrunden og venter derefter på, at begge afslutter.

2. **Vent på en specifik proces:**
   ```sh
   sleep 5 &
   PID=$!
   wait $PID
   echo "Processen med PID $PID er færdig."
   ```
   Her starter vi en `sleep`-kommando, gemmer dens PID, og venter derefter kun på denne specifikke proces.

3. **Vent på den næste baggrundsproces:**
   ```sh
   sleep 5 &
   sleep 3 &
   wait -n
   echo "Den næste baggrundsproces er færdig."
   ```
   I dette eksempel venter vi kun på den næste baggrundsproces, der afslutter, uanset hvilken det er.

## Tips
- Brug `wait` i scripts for at sikre, at alle nødvendige baggrundsprocesser er afsluttet, før scriptet fortsætter.
- Hvis du arbejder med flere baggrundsprocesser, kan det være nyttigt at gemme deres PIDs, så du kan vente på dem individuelt.
- Vær opmærksom på, at `wait` kun fungerer med baggrundsprocesser, så sørg for at starte dem med `&`.