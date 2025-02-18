# [Norsk] Debian Almquist Shell (dash) top bruken: Vise prosessinformasjon

## Oversikt
`top`-kommandoen viser en dynamisk liste over systemprosesser, inkludert informasjon om ressursbruk som CPU og minne. Den oppdateres kontinuerlig, noe som gir et sanntidsbilde av systemets ytelse.

## Bruk
Grunnleggende syntaks for `top`-kommandoen er som følger:

```bash
top [alternativer]
```

## Vanlige alternativer
- `-d <sekunder>`: Angir oppdateringsfrekvensen i sekunder.
- `-n <antall>`: Angir antall oppdateringer før `top` avsluttes.
- `-u <brukernavn>`: Viser kun prosesser som tilhører den spesifiserte brukeren.
- `-p <PID>`: Overvåker kun prosessen med den angitte prosess-ID-en.

## Vanlige eksempler
For å starte `top` med standardinnstillinger, kjør:

```bash
top
```

For å oppdatere visningen hvert 2. sekund:

```bash
top -d 2
```

For å vise prosesser som tilhører en spesifikk bruker, for eksempel "john":

```bash
top -u john
```

For å overvåke en spesifikk prosess med PID 1234:

```bash
top -p 1234
```

For å kjøre `top` i 5 oppdateringer før den avsluttes:

```bash
top -n 5
```

## Tips
- Bruk `h` mens `top` kjører for å få tilgang til hjelpesystemet.
- Trykk `q` for å avslutte `top`-visningen.
- Du kan sortere prosessene ved å trykke på kolonneoverskriftene, for eksempel `P` for CPU-bruk eller `M` for minnebruk.