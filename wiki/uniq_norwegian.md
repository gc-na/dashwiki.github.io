# [Norsk] Debian Almquist Shell (dash) uniq Bruk: Fjerner duplikater fra en sortert liste

## Oversikt
`uniq`-kommandoen brukes til å fjerne duplikater fra en sortert liste med linjer. Den skriver bare ut unike linjer fra en fil eller standard input, noe som gjør den nyttig for å rydde opp i data.

## Bruk
Grunnleggende syntaks for `uniq`-kommandoen er som følger:
```
uniq [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Teller antall forekomster av hver linje.
- `-d`: Viser bare linjer som er duplikater.
- `-u`: Viser bare linjer som er unike.
- `-i`: Ignorerer store og små bokstaver ved sammenligning.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `uniq`:

1. Fjerne duplikater fra en fil:
   ```bash
   uniq fil.txt
   ```

2. Teller antall forekomster av hver linje:
   ```bash
   uniq -c fil.txt
   ```

3. Vise bare duplikater:
   ```bash
   uniq -d fil.txt
   ```

4. Vise bare unike linjer:
   ```bash
   uniq -u fil.txt
   ```

5. Behandle data fra en pipe:
   ```bash
   sort fil.txt | uniq
   ```

## Tips
- Husk at `uniq` bare fjerner påfølgende duplikater, så det er ofte nødvendig å bruke `sort` før `uniq` for å få ønsket resultat.
- Når du bruker `-c`, kan du sortere resultatet for bedre oversikt:
   ```bash
   sort fil.txt | uniq -c | sort -nr
   ```
- Vær oppmerksom på at `uniq` ikke endrer den opprinnelige filen; den skriver bare ut resultatet til standard output.