# [Norsk] Debian Almquist Shell (dash) diff bruk: Sammenlign filer og mapper

## Oversikt
`diff`-kommandoen brukes til å sammenligne innholdet i to filer eller mapper. Den viser forskjellene mellom dem linje for linje, noe som gjør det enkelt å se hva som har blitt endret, lagt til eller fjernet.

## Bruk
Grunnleggende syntaks for `diff`-kommandoen er som følger:

```bash
diff [alternativer] [fil1] [fil2]
```

## Vanlige alternativer
- `-u`: Viser forskjellene i "unified" format, som er mer lesbart.
- `-i`: Ignorerer forskjeller i store og små bokstaver.
- `-w`: Ignorerer forskjeller i hvite tegn.
- `-r`: Sammenligner mapper rekursivt.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `diff` kan brukes:

### Sammenligne to filer
For å sammenligne to tekstfiler, kan du bruke:

```bash
diff fil1.txt fil2.txt
```

### Bruke unified format
For å vise forskjellene i et mer lesbart format:

```bash
diff -u fil1.txt fil2.txt
```

### Ignorere store og små bokstaver
Hvis du vil ignorere forskjeller i bokstavstørrelse:

```bash
diff -i fil1.txt fil2.txt
```

### Sammenligne mapper
For å sammenligne innholdet i to mapper:

```bash
diff -r mappe1/ mappe2/
```

## Tips
- Bruk `-u` alternativet for å få en bedre oversikt over endringene.
- Når du sammenligner mapper, kan `-r` være nyttig for å se alle forskjeller i undermapper.
- Kombiner `-w` og `-i` for å få en mer omfattende sammenligning som ignorerer både hvite tegn og bokstavstørrelse.