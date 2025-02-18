# [Danish] Debian Almquist Shell (dash) jobs brug: Visning af baggrundsopgaver

## Oversigt
`jobs`-kommandoen bruges til at vise en liste over baggrundsopgaver, der kører i den aktuelle shell-session. Det er nyttigt til at holde styr på opgaver, der er blevet sendt til baggrunden, så du kan administrere dem effektivt.

## Brug
Den grundlæggende syntaks for `jobs`-kommandoen er:

```bash
jobs [options] [arguments]
```

## Almindelige muligheder
- `-l`: Viser job-ID'er sammen med jobbeskrivelser.
- `-n`: Viser kun jobs, der er ændret siden den sidste gang `jobs` blev kørt.
- `-p`: Viser kun process-ID'erne for jobs.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `jobs`-kommandoen:

1. **Vis alle baggrundsopgaver:**

   ```bash
   jobs
   ```

2. **Vis baggrundsopgaver med job-ID'er:**

   ```bash
   jobs -l
   ```

3. **Vis kun ændrede baggrundsopgaver:**

   ```bash
   jobs -n
   ```

4. **Vis kun process-ID'er for baggrundsopgaver:**

   ```bash
   jobs -p
   ```

## Tips
- Brug `jobs` regelmæssigt for at holde styr på dine baggrundsopgaver, især når du arbejder med flere opgaver samtidig.
- Kombiner `jobs` med `fg` eller `bg` for at bringe en opgave til forgrunden eller sende den tilbage til baggrunden.
- Husk at jobnummeret, der vises af `jobs`, kan bruges til at referere til specifikke opgaver, når du bruger `fg` eller `bg`.