# [Danish] Debian Almquist Shell (dash) df brug: Viser diskpladsinformation

## Oversigt
`df`-kommandoen bruges til at vise diskpladsinformation for filsystemer på en Unix-lignende operativsystem. Den giver brugeren mulighed for at se, hvor meget plads der er tilgængelig, hvor meget der er brugt, og hvordan filsystemerne er monteret.

## Brug
Den grundlæggende syntaks for `df`-kommandoen er:

```bash
df [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h`: Viser størrelser i et menneskeligt læsbart format (f.eks. KB, MB, GB).
- `-T`: Viser filsystemtypen for hvert monteret filsystem.
- `-a`: Viser alle filsystemer, inklusive dem med 0 brugt plads.
- `-i`: Viser information om inode-brug i stedet for diskplads.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `df`:

1. Vise diskplads for alle monterede filsystemer i et menneskeligt læsbart format:
   ```bash
   df -h
   ```

2. Vise diskplads og filsystemtype:
   ```bash
   df -T
   ```

3. Vise diskplads for et specifikt filsystem (f.eks. `/dev/sda1`):
   ```bash
   df /dev/sda1
   ```

4. Vise alle filsystemer, inklusive dem med 0 brugt plads:
   ```bash
   df -a
   ```

5. Vise inode-brug:
   ```bash
   df -i
   ```

## Tips
- Brug `-h`-muligheden for at gøre output mere læsbart, især når du arbejder med store mængder data.
- Tjek regelmæssigt diskpladsen for at undgå problemer med pladsmangel på servere.
- Kombiner `df` med andre kommandoer som `grep` for at filtrere output og finde specifikke filsystemer.