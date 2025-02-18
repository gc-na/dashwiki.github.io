# [Danish] Debian Almquist Shell (dash) iotop brug: overvågning af disk I/O

## Oversigt
`iotop` er et værktøj til at overvåge disk I/O-aktiviteter i realtid. Det viser, hvilke processer der bruger mest disk I/O, hvilket kan være nyttigt til fejlfinding af ydeevneproblemer på systemet.

## Brug
Den grundlæggende syntaks for `iotop` er:

```bash
iotop [muligheder] [argumenter]
```

## Almindelige muligheder
- `-o`, `--only`: Vis kun processer, der i øjeblikket bruger I/O.
- `-b`, `--batch`: Kør i batch-tilstand, hvilket gør det muligt at køre `iotop` uden at vise en interaktiv grænseflade.
- `-n NUM`, `--iter NUM`: Angiv antallet af iterationer, før `iotop` afsluttes.
- `-d SEC`, `--delay SEC`: Angiv forsinkelsen mellem opdateringer i sekunder.

## Almindelige eksempler
For at se alle processer, der bruger disk I/O, kan du køre:

```bash
iotop
```

For kun at vise processer, der i øjeblikket bruger I/O, kan du bruge:

```bash
iotop -o
```

Hvis du ønsker at køre `iotop` i batch-tilstand og gemme output til en fil, kan du gøre det som følger:

```bash
iotop -b -n 10 > iotop_output.txt
```

For at ændre opdateringsintervallet til 2 sekunder, kan du bruge:

```bash
iotop -d 2
```

## Tips
- Brug `iotop` med `sudo` for at få de mest præcise resultater, da nogle processer kræver root-adgang for at blive vist.
- Overvåg systemets I/O-aktivitet regelmæssigt for at identificere potentielle flaskehalse.
- Kombiner `iotop` med andre værktøjer som `htop` for en mere omfattende systemovervågning.