# [Danish] Debian Almquist Shell (dash) tail brug: Vis de sidste linjer i en fil

## Oversigt
`tail`-kommandoen bruges til at vise de sidste linjer af en fil. Det er nyttigt til at overvåge logfiler eller se de seneste tilføjelser til en tekstfil.

## Brug
Den grundlæggende syntaks for `tail`-kommandoen er:

```bash
tail [muligheder] [argumenter]
```

## Almindelige muligheder
- `-n [antal]`: Angiver antallet af linjer, der skal vises fra slutningen af filen. Standard er 10 linjer.
- `-f`: Følg filen, så nye linjer vises, når de tilføjes. Dette er nyttigt til realtids overvågning af logfiler.
- `-c [antal]`: Viser de sidste [antal] bytes af filen i stedet for linjer.

## Almindelige eksempler
For at vise de sidste 10 linjer af en fil:

```bash
tail filnavn.txt
```

For at vise de sidste 20 linjer af en fil:

```bash
tail -n 20 filnavn.txt
```

For at følge en logfil i realtid:

```bash
tail -f logfil.log
```

For at vise de sidste 100 bytes af en fil:

```bash
tail -c 100 filnavn.txt
```

## Tips
- Brug `-f`-muligheden, når du overvåger logfiler, så du kan se nye indtastninger, mens de tilføjes.
- Kombiner `tail` med `grep` for at filtrere specifikke linjer fra output. For eksempel:

```bash
tail -f logfil.log | grep "fejl"
```

- Hvis du vil se flere linjer end standarden, kan du altid angive et specifikt antal med `-n` for at tilpasse outputtet til dine behov.