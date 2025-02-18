# [Danish] Debian Almquist Shell (dash) tee brug: [kopier output til filer]

## Oversigt
`tee`-kommandoen bruges til at læse standard input og skrive det til både standard output og en eller flere filer. Dette gør det muligt at se output fra en kommando, mens det også gemmes til en fil.

## Brug
Den grundlæggende syntaks for `tee`-kommandoen er:

```bash
tee [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`, `--append`: Tilføj output til slutningen af filen i stedet for at overskrive den.
- `-i`, `--ignore-interrupts`: Ignorer signaler, der kan afbryde kommandoen.
- `--help`: Vis hjælp og afslut.
- `--version`: Vis versionen af `tee`.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `tee`:

1. **Gem output til en fil:**
   ```bash
   echo "Hej verden" | tee output.txt
   ```

2. **Tilføj output til en eksisterende fil:**
   ```bash
   echo "Endnu en linje" | tee -a output.txt
   ```

3. **Brug `tee` med en pipelining:**
   ```bash
   ls -l | tee filoversigt.txt | grep "d"
   ```

4. **Skrive til flere filer:**
   ```bash
   echo "Data til flere filer" | tee fil1.txt fil2.txt
   ```

## Tips
- Brug `-a`-muligheden, når du ønsker at bevare eksisterende indhold i en fil og blot tilføje ny data.
- Kombiner `tee` med andre kommandoer i en pipeline for at analysere output, mens du gemmer det.
- Vær opmærksom på filrettigheder; sørg for, at du har de nødvendige tilladelser til at skrive til de filer, du angiver.