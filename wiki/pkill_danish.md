# [Danish] Debian Almquist Shell (dash) pkill brug: Dræb processer baseret på navn

## Oversigt
`pkill`-kommandoen bruges til at dræbe processer baseret på deres navn eller andre egenskaber. Dette gør det muligt at stoppe en eller flere kørende processer uden at skulle finde deres proces-id (PID).

## Brug
Den grundlæggende syntaks for `pkill`-kommandoen er som følger:

```bash
pkill [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`: Matcher mod hele kommandolinjen i stedet for kun procesnavnet.
- `-n`: Dræber den nyeste proces, der matcher kriterierne.
- `-o`: Dræber den ældste proces, der matcher kriterierne.
- `-signal`: Angiver det signal, der skal sendes til processen (standard er SIGTERM).

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `pkill`:

1. Dræb alle processer med navnet "firefox":
   ```bash
   pkill firefox
   ```

2. Dræb alle processer, der matcher "python":
   ```bash
   pkill python
   ```

3. Dræb den nyeste proces med navnet "myapp":
   ```bash
   pkill -n myapp
   ```

4. Dræb alle processer, der matcher "backup" ved at bruge hele kommandolinjen:
   ```bash
   pkill -f backup
   ```

5. Send et SIGKILL-signal til alle processer med navnet "node":
   ```bash
   pkill -9 node
   ```

## Tips
- Brug `pkill -l` for at se en liste over tilgængelige signaler, som du kan sende til processer.
- Vær forsigtig med at bruge `pkill` uden specifikation, da det kan dræbe flere processer, end du havde til hensigt.
- Overvej at bruge `pgrep` til først at kontrollere, hvilke processer der vil blive dræbt, før du bruger `pkill`.