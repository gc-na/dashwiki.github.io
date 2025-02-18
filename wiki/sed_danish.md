# [Danish] Debian Almquist Shell (dash) sed Brug: Rediger tekststrømme

## Oversigt
`sed` (stream editor) er et kraftfuldt værktøj til at manipulere tekststrømme. Det bruges ofte til at søge, erstatte, indsætte eller slette tekst i filer eller inputstrømme, hvilket gør det uundgåeligt i mange shell-scripts og tekstbehandlingsopgaver.

## Brug
Den grundlæggende syntaks for `sed` er som følger:

```bash
sed [muligheder] [argumenter]
```

## Almindelige muligheder
- `-e`: Angiver en kommando, der skal udføres.
- `-i`: Ændrer filen direkte (in-place).
- `-n`: Undertrykker standard output; bruges ofte sammen med `p` for at udskrive specifikke linjer.
- `s`: Erstatningskommando, der bruges til at søge og erstatte tekst.

## Almindelige eksempler

### Erstatte tekst i en fil
For at erstatte "kat" med "hund" i en fil kaldet `dyr.txt`, kan du bruge:

```bash
sed -i 's/kat/hund/g' dyr.txt
```

### Udskrive specifikke linjer
For at udskrive linje 2 i en fil:

```bash
sed -n '2p' fil.txt
```

### Fjerne tomme linjer
For at fjerne alle tomme linjer fra en fil:

```bash
sed -i '/^$/d' fil.txt
```

### Indsætte tekst før en bestemt linje
For at indsætte teksten "Ny linje" før linje 3:

```bash
sed -i '3i Ny linje' fil.txt
```

## Tips
- Brug `-n` sammen med `p` for kun at vise de linjer, du er interesseret i.
- Test dine `sed`-kommandoer uden `-i` først for at sikre, at de fungerer som forventet, før du ændrer filer permanent.
- Læs `sed`-manualen (`man sed`) for at få en dybere forståelse af alle tilgængelige muligheder og syntaks.