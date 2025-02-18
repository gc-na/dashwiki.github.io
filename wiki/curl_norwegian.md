# [Norsk] Debian Almquist Shell (dash) curl bruk: Hente data fra nettverk

## Oversikt
`curl` er et kommandolinjeverktøy som brukes til å overføre data fra eller til en server ved hjelp av ulike protokoller, inkludert HTTP, HTTPS, FTP, og mer. Det er et nyttig verktøy for å hente innhold fra nettadresser eller sende data til servere.

## Bruk
Den grunnleggende syntaksen for `curl` er som følger:

```bash
curl [alternativer] [argumenter]
```

## Vanlige alternativer
- `-O`: Laster ned filen og lagrer den med det samme navnet som på serveren.
- `-o [filnavn]`: Laster ned filen og lagrer den med et spesifisert filnavn.
- `-I`: Henter bare HTTP-headerne fra en URL.
- `-d [data]`: Sender data til serveren (vanligvis brukt med POST-forespørsel).
- `-H [header]`: Legger til en spesifisert HTTP-header i forespørselen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `curl` kan brukes:

### Hente en webside
```bash
curl https://www.example.com
```

### Laste ned en fil
```bash
curl -O https://www.example.com/fil.zip
```

### Laste ned en fil med et spesifisert navn
```bash
curl -o minfil.zip https://www.example.com/fil.zip
```

### Hente bare HTTP-headerne
```bash
curl -I https://www.example.com
```

### Sende data med POST-forespørsel
```bash
curl -d "navn=Ola&alder=30" https://www.example.com/submit
```

### Legge til en HTTP-header
```bash
curl -H "Authorization: Bearer token" https://www.example.com/protected
```

## Tips
- Bruk `-v` for å se detaljer om forespørselen og svaret, noe som kan være nyttig for feilsøking.
- For å følge omdirigeringer, legg til `-L` alternativet.
- Vær oppmerksom på at `curl` kan håndtere både GET og POST forespørsel, avhengig av hvordan du bruker det.
- Sjekk alltid dokumentasjonen med `man curl` for mer informasjon om tilgjengelige alternativer og bruksområder.