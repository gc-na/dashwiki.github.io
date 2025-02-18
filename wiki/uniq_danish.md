# [Danish] Debian Almquist Shell (dash) uniq Brug: Fjerner duplikater fra en sorteret liste

## Oversigt
`uniq`-kommandoen bruges til at fjerne eller rapportere duplikerede linjer fra en sorteret tekstfil. Den er nyttig, når du har brug for at rense data ved at eliminere gentagne indgange.

## Brug
Den grundlæggende syntaks for `uniq`-kommandoen er:

```
uniq [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c`: Tæller antallet af forekomster af hver unik linje.
- `-d`: Viser kun de linjer, der er duplikeret.
- `-u`: Viser kun de linjer, der er unikke (ikke duplikerede).
- `-i`: Ignorerer forskelle mellem store og små bogstaver.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `uniq`:

1. Fjerne duplikater fra en fil:
   ```bash
   sort fil.txt | uniq
   ```

2. Tælle antallet af hver unik linje:
   ```bash
   sort fil.txt | uniq -c
   ```

3. Vise kun de linjer, der er duplikeret:
   ```bash
   sort fil.txt | uniq -d
   ```

4. Vise kun unikke linjer:
   ```bash
   sort fil.txt | uniq -u
   ```

5. Ignorere store og små bogstaver:
   ```bash
   sort fil.txt | uniq -i
   ```

## Tips
- Sørg for, at inputfilen er sorteret, da `uniq` kun fjerner på hinanden følgende duplikater.
- Brug `sort`-kommandoen før `uniq` for at sikre, at alle duplikater bliver fjernet.
- Kombiner `uniq` med andre kommandoer ved hjælp af rør (`|`) for at skabe mere komplekse databehandlingsstrømme.