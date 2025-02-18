# [Danish] Debian Almquist Shell (dash) ved at: planlægge opgaver

## Oversigt
`at`-kommandoen bruges til at planlægge en opgave, der skal udføres på et bestemt tidspunkt i fremtiden. Det er nyttigt til at køre scripts eller kommandoer, når det passer dig.

## Brug
Den grundlæggende syntaks for `at`-kommandoen er:

```bash
at [options] [arguments]
```

## Almindelige muligheder
- `-f`: Angiver en fil, der indeholder de kommandoer, der skal køres.
- `-m`: Sender en mail til brugeren, når opgaven er udført.
- `-q`: Angiver en kø, som opgaven skal tilføjes til (f.eks. a, b, c).
- `-l`: Viser en liste over planlagte opgaver.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `at`:

1. Planlæg en opgave til at køre nu + 1 time:
   ```bash
   echo "backup.sh" | at now + 1 hour
   ```

2. Kør en kommando på et bestemt tidspunkt:
   ```bash
   echo "echo 'Hello, World!'" | at 14:00
   ```

3. Brug en fil til at angive kommandoer:
   ```bash
   at -f /path/to/script.sh 09:00
   ```

4. Vis en liste over planlagte opgaver:
   ```bash
   at -l
   ```

## Tips
- Sørg for, at `atd`-tjenesten kører, da den er nødvendig for at planlægge opgaver.
- Brug `-m`-muligheden, hvis du ønsker at modtage en bekræftelse via e-mail, når opgaven er udført.
- Tjek systemets tidsindstillinger for at sikre, at opgaverne kører på det ønskede tidspunkt.