# [Danish] Debian Almquist Shell (dash) ulimit brug: Justering af systemressourcer

## Oversigt
`ulimit`-kommandoen bruges til at indstille eller vise grænser for systemressourcer for den aktuelle shell-session. Dette kan være nyttigt for at forhindre, at et program bruger for mange ressourcer og dermed påvirker systemets stabilitet.

## Brug
Den grundlæggende syntaks for `ulimit`-kommandoen er:

```sh
ulimit [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`: Viser alle nuværende grænser.
- `-c`: Sætter grænsen for størrelsen af core-dumps.
- `-d`: Sætter grænsen for størrelsen af det virtuelle hukommelsesområde.
- `-f`: Sætter grænsen for størrelsen af filer, der kan oprettes.
- `-l`: Sætter grænsen for størrelsen af låst hukommelse.
- `-m`: Sætter grænsen for den fysiske hukommelse.
- `-n`: Sætter grænsen for antallet af åbne filer.
- `-s`: Sætter stakken størrelse.
- `-t`: Sætter grænsen for CPU-tid i sekunder.
- `-v`: Sætter grænsen for størrelsen af det virtuelle hukommelsesområde.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `ulimit`:

1. Vise alle nuværende grænser:
   ```sh
   ulimit -a
   ```

2. Sætte grænsen for antallet af åbne filer til 1024:
   ```sh
   ulimit -n 1024
   ```

3. Sætte grænsen for størrelsen af core-dumps til 0 (deaktiver core-dumps):
   ```sh
   ulimit -c 0
   ```

4. Sætte grænsen for CPU-tid til 60 sekunder:
   ```sh
   ulimit -t 60
   ```

5. Vise grænsen for størrelsen af filer, der kan oprettes:
   ```sh
   ulimit -f
   ```

## Tips
- Tjek altid de nuværende grænser med `ulimit -a`, før du ændrer dem.
- Vær forsigtig med at sætte grænser for lavt, da det kan forhindre programmer i at køre korrekt.
- Ændringer foretaget med `ulimit` gælder kun for den aktuelle shell-session og vil ikke påvirke andre sessioner eller systemet som helhed.