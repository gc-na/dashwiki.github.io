# [Norsk] Debian Almquist Shell (dash) sed Bruk: Endre tekst i filer

## Oversikt
`sed` (stream editor) er et kraftig verktøy for tekstbehandling i Unix-lignende operativsystemer. Det brukes primært til å utføre grunnleggende tekstmanipulering, som å erstatte, slette eller legge til tekst i filer eller strenger.

## Bruk
Grunnleggende syntaks for `sed` er som følger:

```bash
sed [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e`: Angir en kommando til å bli utført.
- `-i`: Endrer filen på stedet (in-place).
- `-n`: Undertrykker automatisk utskrift av linjer, brukes sammen med `p` for å skrive ut spesifikke linjer.
- `s`: Brukes for å erstatte tekst.

## Vanlige eksempler

### Erstatte tekst i en fil
For å erstatte "gammel" med "ny" i en fil:

```bash
sed 's/gammel/ny/' fil.txt
```

### Erstatte tekst og lagre endringer i filen
For å erstatte "gammel" med "ny" og lagre endringene:

```bash
sed -i 's/gammel/ny/' fil.txt
```

### Slette linjer som inneholder et bestemt mønster
For å slette linjer som inneholder "fjern meg":

```bash
sed '/fjern meg/d' fil.txt
```

### Skrive ut spesifikke linjer
For å skrive ut linje 2 og 4 fra en fil:

```bash
sed -n '2p; 4p' fil.txt
```

## Tips
- Bruk `-i.bak` for å lage en sikkerhetskopi av filen før du gjør endringer.
- Test kommandoene dine uten `-i` først for å se resultatet før du endrer filen.
- Kombiner flere `sed`-kommandoer ved å bruke `-e` for å utføre flere operasjoner i én linje.