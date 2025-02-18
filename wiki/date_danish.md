# [Danish] Debian Almquist Shell (dash) date: [viser dato og tid]

## Oversigt
`date`-kommandoen bruges til at vise og ændre systemets dato og tid. Den kan også formatere dato og tid i forskellige formater, hvilket gør den nyttig til scripting og automatisering.

## Brug
Den grundlæggende syntaks for `date`-kommandoen er:

```bash
date [muligheder] [argumenter]
```

## Almindelige muligheder
- `+FORMAT`: Angiver et brugerdefineret format for output.
- `-u`: Viser dato og tid i UTC (Coordinated Universal Time).
- `-d STRING`: Angiver en dato og tid baseret på en given streng.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `date`-kommandoen:

1. Vise den aktuelle dato og tid:
   ```bash
   date
   ```

2. Vise dato og tid i UTC:
   ```bash
   date -u
   ```

3. Vise datoen i et specifikt format (f.eks. År-Måned-Dag):
   ```bash
   date +"%Y-%m-%d"
   ```

4. Vise datoen for en given streng (f.eks. "næste fredag"):
   ```bash
   date -d "next Friday"
   ```

5. Vise tid i 12-timers format:
   ```bash
   date +"%I:%M %p"
   ```

## Tips
- Brug `man date` for at få en detaljeret manual om `date`-kommandoen og dens muligheder.
- Eksperimenter med forskellige formatstrenge for at tilpasse output til dine behov.
- Husk, at ændringer i systemets dato og tid kan kræve administrative rettigheder.