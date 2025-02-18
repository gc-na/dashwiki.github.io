# [Danish] Debian Almquist Shell (dash) batch brug: Kør batchjob

## Oversigt
`batch`-kommandoen bruges til at planlægge opgaver, der skal køres på et senere tidspunkt, når systemet er mindre belastet. Det giver brugerne mulighed for at indtaste kommandoer, der vil blive udført, når systemet har ledige ressourcer.

## Brug
Den grundlæggende syntaks for `batch`-kommandoen er:

```bash
batch [options] [arguments]
```

## Almindelige muligheder
- `-f`: Angiv en fil, der indeholder kommandoer, der skal køres.
- `-q`: Kør i stille tilstand, uden at vise output.
- `-h`: Vis hjælp og afslut.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `batch`:

1. Kør en enkel kommando, når systemet er ledigt:
   ```bash
   echo "echo 'Hello, World!'" | batch
   ```

2. Kør et script ved at angive en fil:
   ```bash
   batch < my_script.sh
   ```

3. Kør en kommando i stille tilstand:
   ```bash
   echo "backup.sh" | batch -q
   ```

## Tips
- Sørg for at kontrollere systemets belastning, før du planlægger batchjob, for at sikre, at de kører på det rigtige tidspunkt.
- Brug `atq`-kommandoen til at se en liste over planlagte job.
- Overvej at bruge `batch` til opgaver, der kræver betydelig beregningskraft, så de ikke påvirker brugerens oplevelse.