# [Danish] Debian Almquist Shell (dash) printf brug: Formatere og udskrive tekst

## Oversigt
`printf`-kommandoen bruges til at formatere og udskrive tekst til standard output. Den tilbyder mere kontrol over outputformatet end den enklere `echo`-kommando, hvilket gør den nyttig til at generere præcise og strukturerede udskrifter.

## Brug
Den grundlæggende syntaks for `printf`-kommandoen er som følger:

```sh
printf [options] [arguments]
```

## Almindelige muligheder
- `-v var`: Tildel output til en variabel i stedet for at udskrive det.
- `--help`: Vis en hjælpetekst med en liste over muligheder.
- `--version`: Vis versionsoplysninger for `printf`.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `printf` kan bruges:

1. **Enkel tekstudskrift:**
   ```sh
   printf "Hej, verden!\n"
   ```

2. **Formateret udskrift med variabler:**
   ```sh
   navn="Alice"
   alder=30
   printf "%s er %d år gammel.\n" "$navn" "$alder"
   ```

3. **Udskrive tal med decimaler:**
   ```sh
   printf "Pi er cirka %.2f\n" 3.14159
   ```

4. **Udskrive en tabel:**
   ```sh
   printf "%-10s %-10s\n" "Navn" "Alder"
   printf "%-10s %-10d\n" "Bob" 25
   printf "%-10s %-10d\n" "Charlie" 35
   ```

## Tips
- Brug `\n` for at tilføje nye linjer i output.
- Vær opmærksom på formatstrenge; de bestemmer, hvordan argumenterne bliver præsenteret.
- `printf` er mere pålidelig end `echo`, især når det kommer til specialtegn og formatering.