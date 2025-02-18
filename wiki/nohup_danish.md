# [Danish] Debian Almquist Shell (dash) nohup brug: Kør kommandoer uden at blive påvirket af logout

## Oversigt
`nohup` (no hang up) er et værktøj, der gør det muligt at køre kommandoer i baggrunden, selv når brugeren logger ud af systemet. Det sikrer, at processen fortsætter med at køre, selvom terminalen lukkes.

## Brug
Den grundlæggende syntaks for `nohup` er som følger:

```bash
nohup [muligheder] [argumenter]
```

## Almindelige muligheder
- `&`: Kør kommandoen i baggrunden.
- `-h`: Vis hjælp til brug af `nohup`.
- `-p`: Angiv en proces-ID til at køre `nohup` med.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `nohup`:

1. Kør et script i baggrunden:
   ```bash
   nohup ./mit_script.sh &
   ```

2. Kør en langvarig opgave og gem output til en fil:
   ```bash
   nohup long_running_command > output.log &
   ```

3. Kør en Python-applikation uden at blive påvirket af logout:
   ```bash
   nohup python3 min_applikation.py &
   ```

## Tips
- Brug `&` for at sikre, at kommandoen kører i baggrunden.
- Tjek `nohup.out` for output, hvis du ikke angiver en outputfil.
- Overvej at bruge `screen` eller `tmux` til mere komplekse sessioner, hvor du ønsker at interagere med processen senere.