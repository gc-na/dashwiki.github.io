# [Danish] Debian Almquist Shell (dash) crontab brug: Planlægning af opgaver

## Oversigt
`crontab`-kommandoen bruges til at planlægge og automatisere opgaver på et Unix-lignende system. Den giver brugerne mulighed for at køre scripts eller kommandoer på bestemte tidspunkter eller med faste intervaller.

## Brug
Den grundlæggende syntaks for `crontab`-kommandoen er som følger:

```bash
crontab [muligheder] [argumenter]
```

## Almindelige muligheder
- `-e`: Rediger den nuværende crontab for den bruger, der er logget ind.
- `-l`: Vis den nuværende crontab for den bruger, der er logget ind.
- `-r`: Slet den nuværende crontab for den bruger, der er logget ind.
- `-i`: Bekræft sletning af crontab, når `-r` bruges.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `crontab`:

1. **Rediger crontab**:
   For at redigere din crontab, kan du bruge:
   ```bash
   crontab -e
   ```

2. **Vis nuværende crontab**:
   For at se dine nuværende planlagte opgaver:
   ```bash
   crontab -l
   ```

3. **Slet crontab**:
   For at slette din crontab:
   ```bash
   crontab -r
   ```

4. **Planlæg en opgave**:
   For at køre et script hver dag kl. 2 om natten, kan du tilføje følgende linje i din crontab:
   ```bash
   0 2 * * * /path/to/your/script.sh
   ```

5. **Kør en kommando hvert 15. minut**:
   For at køre en kommando hvert 15. minut, kan du bruge:
   ```bash
   */15 * * * * /path/to/your/command
   ```

## Tips
- Sørg for, at dine scripts har de nødvendige tilladelser til at køre.
- Brug fulde stier til kommandoer og scripts for at undgå problemer med miljøvariabler.
- Tjek logfilerne for at se output fra dine cron-jobs, hvis de ikke kører som forventet.