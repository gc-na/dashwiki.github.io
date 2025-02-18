# [Danish] Debian Almquist Shell (dash) ps Brug: Vis processer i systemet

## Oversigt
`ps`-kommandoen bruges til at vise aktive processer i systemet. Den giver information om de kørende processer, såsom proces-id (PID), brugernavn, CPU-forbrug og meget mere.

## Brug
Den grundlæggende syntaks for `ps`-kommandoen er:

```bash
ps [muligheder] [argumenter]
```

## Almindelige muligheder
- `-e` eller `-A`: Vis alle processer.
- `-f`: Vis fuld format med detaljer om processerne.
- `-u`: Vis processer for en specifik bruger.
- `-l`: Vis detaljeret liste over processer.
- `-p <PID>`: Vis information om en specifik proces ved hjælp af dens PID.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `ps`-kommandoen:

1. Vis alle kørende processer:
   ```bash
   ps -e
   ```

2. Vis processer med fuld format:
   ```bash
   ps -f
   ```

3. Vis processer for en specifik bruger:
   ```bash
   ps -u brugernavn
   ```

4. Vis detaljeret liste over processer:
   ```bash
   ps -l
   ```

5. Vis information om en specifik proces (f.eks. PID 1234):
   ```bash
   ps -p 1234
   ```

## Tips
- Brug `ps aux` for at få en omfattende liste over alle processer med detaljer om brugere og ressourcer.
- Kombiner `ps` med `grep` for at finde specifikke processer, f.eks.:
  ```bash
  ps -e | grep bash
  ```
- Overvej at bruge `top`-kommandoen for en dynamisk visning af processerne i realtid.