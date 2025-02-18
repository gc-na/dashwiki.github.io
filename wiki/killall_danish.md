# [Dansk] Debian Almquist Shell (dash) killall brug: Dræb processer ved navn

## Oversigt
`killall`-kommandoen bruges til at dræbe alle processer, der kører med et bestemt navn. Dette er nyttigt, når du ønsker at stoppe alle instanser af et program uden at skulle finde og dræbe hver enkelt proces manuelt.

## Brug
Den grundlæggende syntaks for `killall`-kommandoen er:

```bash
killall [muligheder] [argumenter]
```

## Almindelige muligheder
- `-u, --user <bruger>`: Dræb kun processer, der tilhører den angivne bruger.
- `-s, --signal <signal>`: Angiv det signal, der skal sendes til processerne (standard er SIGTERM).
- `-q, --quiet`: Undertrykkelse af fejlmeddelelser, hvis ingen processer blev dræbt.
- `-I, --ignore-case`: Ignorer store og små bogstaver, når du angiver procesnavnet.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `killall`:

1. Dræb alle instanser af `firefox`:
   ```bash
   killall firefox
   ```

2. Dræb alle `python3`-processer:
   ```bash
   killall python3
   ```

3. Dræb en specifik proces med et signal (f.eks. SIGKILL):
   ```bash
   killall -s SIGKILL firefox
   ```

4. Dræb processer, der tilhører en bestemt bruger:
   ```bash
   killall -u brugernavn firefox
   ```

5. Ignorer store og små bogstaver, når du dræber `Chrome`:
   ```bash
   killall -I chrome
   ```

## Tips
- Vær forsigtig, når du bruger `killall`, da det dræber alle processer med det angivne navn, hvilket kan påvirke systemets stabilitet, hvis du dræber kritiske processer.
- Brug `killall -q` for at undgå unødvendige fejlmeddelelser, hvis ingen processer er aktive.
- Overvej at bruge `pgrep` til at finde processer, før du dræber dem, for at sikre, at du ikke dræber de forkerte processer.