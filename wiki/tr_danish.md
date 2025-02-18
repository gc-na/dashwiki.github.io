# [Danish] Debian Almquist Shell (dash) tr: [omdanne tegn]

## Oversigt
`tr`-kommandoen bruges til at omdanne eller slette tegn i inputdata. Den læser fra standard input og kan ændre tegn i tekststrømme, hvilket gør den nyttig til tekstbehandling.

## Brug
Den grundlæggende syntaks for `tr`-kommandoen er:

```bash
tr [muligheder] [argumenter]
```

## Almindelige muligheder
- `-d`: Sletter de angivne tegn fra input.
- `-s`: Komprimerer gentagne tegn til et enkelt tegn.
- `-c`: Angiver, at de angivne tegn skal anvendes som en komplementær liste.

## Almindelige eksempler

1. **Erstatte små bogstaver med store bogstaver:**
   ```bash
   echo "hej verden" | tr 'a-z' 'A-Z'
   ```

2. **Slette specifikke tegn:**
   ```bash
   echo "hej verden!" | tr -d '!'
   ```

3. **Komprimere gentagne mellemrum:**
   ```bash
   echo "hej    verden" | tr -s ' '
   ```

4. **Omdanne tegn til deres komplement:**
   ```bash
   echo "abc" | tr -c 'a-z' 'X'
   ```

## Tips
- Brug `tr` i kombination med andre kommandoer ved hjælp af rør (`|`) for at opnå mere komplekse tekstbehandlingsopgaver.
- Vær opmærksom på, at `tr` kun arbejder med enkelttegn og ikke med strenge.
- Test altid dine kommandoer med en prøveinput for at sikre, at de fungerer som forventet, før du anvender dem på større datasæt.