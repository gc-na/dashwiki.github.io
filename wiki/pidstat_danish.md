# [Danish] Debian Almquist Shell (dash) pidstat brug: Overvågning af processtatistik

## Oversigt
`pidstat` er et værktøj, der bruges til at overvåge og rapportere statistikker om systemprocesser. Det giver information om CPU-forbrug, hukommelsesforbrug og andre ressourceanvendelser for aktive processer.

## Brug
Den grundlæggende syntaks for `pidstat`-kommandoen er som følger:

```bash
pidstat [options] [arguments]
```

## Almindelige muligheder
- `-h`: Vis hjælp og afslut.
- `-r`: Vis hukommelsesstatistik.
- `-u`: Vis CPU-brugsstatistik.
- `-p <pid>`: Angiv specifik proces-ID for overvågning.
- `-t`: Vis trådstatistik for processer.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `pidstat`:

1. **Overvågning af CPU-forbrug for alle processer**:
   ```bash
   pidstat -u 1
   ```
   Dette viser CPU-brugsstatistik for alle processer hvert sekund.

2. **Visning af hukommelsesforbrug for en specifik proces**:
   ```bash
   pidstat -r -p 1234 1
   ```
   Her overvåges hukommelsesforbruget for processen med PID 1234 hvert sekund.

3. **Overvågning af både CPU- og hukommelsesstatistik**:
   ```bash
   pidstat -u -r 1
   ```
   Dette viser både CPU- og hukommelsesstatistik for alle processer hvert sekund.

4. **Visning af trådstatistik for en specifik proces**:
   ```bash
   pidstat -t -p 5678 1
   ```
   Her overvåges trådstatistik for processen med PID 5678 hvert sekund.

## Tips
- Brug `pidstat` sammen med `grep` for at filtrere specifikke processer, f.eks. `pidstat -u | grep myprocess`.
- Overvej at køre `pidstat` i baggrunden, hvis du overvåger systemet i længere tid, så du kan analysere dataene senere.
- Kombiner `pidstat` med andre værktøjer som `top` eller `htop` for en mere omfattende overvågning af systemressourcer.