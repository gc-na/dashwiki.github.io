# [Dansk] Debian Almquist Shell (dash) free: Vis hukommelsesforbrug

## Oversigt
`free`-kommandoen bruges til at vise information om systemets hukommelsesforbrug, herunder både RAM og swap-hukommelse. Det giver et hurtigt overblik over, hvor meget hukommelse der er i brug, og hvor meget der er tilgængeligt.

## Brug
Den grundlæggende syntaks for `free`-kommandoen er:

```bash
free [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h`: Viser hukommelsesstørrelser i et menneskeligt læsbart format (f.eks. MB eller GB).
- `-m`: Viser hukommelse i megabyte.
- `-g`: Viser hukommelse i gigabyte.
- `-s [sekunder]`: Opdaterer visningen med det angivne tidsinterval i sekunder.
- `-t`: Viser en total række for både RAM og swap.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `free`-kommandoen:

1. Vis hukommelsesforbrug i standardformat:
   ```bash
   free
   ```

2. Vis hukommelsesforbrug i et menneskeligt læsbart format:
   ```bash
   free -h
   ```

3. Vis hukommelse i megabyte:
   ```bash
   free -m
   ```

4. Opdater visningen hvert 5. sekund:
   ```bash
   free -s 5
   ```

5. Vis total hukommelse for RAM og swap:
   ```bash
   free -t
   ```

## Tips
- Brug `-h` muligheden for at gøre output mere læsbart, især når du arbejder med store mængder hukommelse.
- Kombiner `free` med `watch` for at overvåge hukommelsesforbruget i realtid:
  ```bash
  watch free -h
  ```
- Tjek regelmæssigt hukommelsesforbruget for at identificere potentielle problemer med systemets ydeevne.