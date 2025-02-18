# [Danish] Debian Almquist Shell (dash) time brug: Mål kommandotid

## Oversigt
`time`-kommandoen bruges til at måle, hvor lang tid en given kommando tager at udføre. Den giver information om den samlede tid, der er brugt, samt opdeling af CPU-tid og realtid.

## Brug
Den grundlæggende syntaks for `time`-kommandoen er:

```bash
time [options] [arguments]
```

## Almindelige muligheder
- `-p`: Udskriver tiden i et mere menneskeligt læsbart format.
- `-o FILE`: Gemmer outputtet i den angivne fil i stedet for at vise det på skærmen.
- `-v`: Viser detaljeret information om ressourceforbruget.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `time`-kommandoen:

1. Mål tiden for at køre et script:
   ```bash
   time ./mit_script.sh
   ```

2. Mål tiden for at køre en kommando og gem output i en fil:
   ```bash
   time -o tid.txt ls -l
   ```

3. Brug `-p` for at få et mere simpelt output:
   ```bash
   time -p sleep 2
   ```

4. Få detaljeret information om en kommando:
   ```bash
   time -v find / -name "*.txt"
   ```

## Tips
- Brug `time` til at optimere scripts ved at identificere langsomme kommandoer.
- Gem outputtet i en fil, hvis du skal analysere resultaterne senere.
- Vær opmærksom på, at `time` kan have forskellige implementeringer; sørg for at bruge den rigtige syntaks for din shell.