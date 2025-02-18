# [Norsk] Debian Almquist Shell (dash) wget bruk: Hente filer fra nettet

## Oversikt
`wget` er et kraftig kommandolinjeverktøy som brukes til å laste ned filer fra internett. Det støtter HTTP, HTTPS og FTP-protokoller, og kan håndtere både enkle og komplekse nedlastingsoppgaver.

## Bruk
Grunnleggende syntaks for `wget`-kommandoen er som følger:

```bash
wget [alternativer] [argumenter]
```

## Vanlige alternativer
- `-O <filnavn>`: Angi et spesifikt filnavn for den nedlastede filen.
- `-c`: Fortsett en avbrutt nedlasting.
- `-q`: Kjør i stille modus, uten utdata til terminalen.
- `--limit-rate=<hastighet>`: Sett en grense for nedlastingshastigheten.
- `-r`: Aktiver rekursiv nedlasting.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `wget`:

### Last ned en enkelt fil
```bash
wget https://example.com/fil.txt
```

### Last ned en fil med spesifisert filnavn
```bash
wget -O nyfil.txt https://example.com/fil.txt
```

### Fortsett en avbrutt nedlasting
```bash
wget -c https://example.com/fil.txt
```

### Last ned en hel nettside rekursivt
```bash
wget -r https://example.com
```

### Sett en grense for nedlastingshastigheten
```bash
wget --limit-rate=100k https://example.com/fil.txt
```

## Tips
- Bruk `-q` for å unngå unødvendig utdata når du laster ned mange filer.
- Kombiner `-c` med `-r` for å fortsette nedlastinger av store nettsteder.
- Vær oppmerksom på nettstedets retningslinjer for nedlasting for å unngå å overbelaste serveren.