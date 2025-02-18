# [Danish] Debian Almquist Shell (dash) cal Brug: Vis kalender

## Oversigt
`cal`-kommandoen bruges til at vise en kalender i terminalen. Den kan vise månedlige eller årlige kalendere og giver en hurtig måde at se datoer og uger på.

## Brug
Den grundlæggende syntaks for `cal`-kommandoen er:

```bash
cal [options] [arguments]
```

## Almindelige muligheder
- `-m`: Vis kalenderen med den nuværende måned som standard.
- `-y`: Vis kalenderen for det aktuelle år.
- `-3`: Vis den nuværende måned, samt måneden før og efter.
- `-1`: Vis kalenderen for den specifikke måned (standard).
- `-j`: Vis kalenderen med julianer datoer.

## Almindelige eksempler
For at vise den nuværende måned:

```bash
cal
```

For at vise kalenderen for et specifikt år, f.eks. 2023:

```bash
cal 2023
```

For at vise kalenderen for oktober 2023:

```bash
cal 10 2023
```

For at vise den nuværende måned sammen med måneden før og efter:

```bash
cal -3
```

For at vise kalenderen med julianer datoer:

```bash
cal -j
```

## Tips
- Brug `cal -y` for hurtigt at få et overblik over hele året.
- Kombiner `cal` med `grep` for at finde specifikke datoer eller uger.
- Du kan også bruge `cal` i scripts for at generere kalendere automatisk.