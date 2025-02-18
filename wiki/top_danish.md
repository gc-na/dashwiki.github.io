# [Danish] Debian Almquist Shell (dash) top kommando: Vis systemprocesser i realtid

## Oversigt
`top` kommandoen bruges til at vise systemets aktive processer i realtid. Den giver en dynamisk visning af, hvilke processer der bruger mest CPU og hukommelse, hvilket gør det til et nyttigt værktøj til overvågning af systemets ydeevne.

## Brug
Den grundlæggende syntaks for `top` kommandoen er:

```bash
top [options]
```

## Almindelige muligheder
- `-d <sekunder>`: Angiver opdateringsintervallet i sekunder.
- `-n <antal>`: Angiver, hvor mange gange `top` skal opdatere visningen, før den afsluttes.
- `-b`: Kører `top` i batch-tilstand, hvilket er nyttigt til at gemme output til en fil.

## Almindelige eksempler
For at starte `top` med standardindstillingerne, kan du blot skrive:

```bash
top
```

For at ændre opdateringsintervallet til 2 sekunder, kan du bruge:

```bash
top -d 2
```

Hvis du ønsker at køre `top` i batch-tilstand og gemme output til en fil, kan du gøre det sådan:

```bash
top -b -n 5 > output.txt
```

## Tips
- Brug `h` inden for `top` for at få hjælp til de forskellige tastaturgenveje.
- Tryk på `M` for at sortere processerne efter hukommelsesforbrug.
- Tryk på `P` for at sortere efter CPU-forbrug.