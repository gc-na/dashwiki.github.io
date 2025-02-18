# [Norsk] Debian Almquist Shell (dash) ftp bruk: Overfør filer mellom datamaskiner

## Oversikt
`ftp`-kommandoen brukes til å overføre filer mellom datamaskiner over et nettverk ved hjelp av File Transfer Protocol (FTP). Den lar brukere koble til en FTP-server for å laste opp eller laste ned filer.

## Bruk
Grunnleggende syntaks for `ftp`-kommandoen er som følger:

```bash
ftp [alternativer] [server]
```

## Vanlige alternativer
- `-v`: Aktiverer verbose-modus, som viser mer detaljert informasjon om overføringen.
- `-n`: Deaktiverer automatisk innlogging.
- `-i`: Deaktiverer interaktiv modus, som gjør at flere filer kan overføres uten bekreftelse for hver fil.

## Vanlige eksempler

### Koble til en FTP-server
For å koble til en FTP-server, bruk følgende kommando:

```bash
ftp ftp.example.com
```

### Laste ned en fil
For å laste ned en fil fra serveren, bruk `get`-kommandoen:

```bash
get filnavn.txt
```

### Laste opp en fil
For å laste opp en fil til serveren, bruk `put`-kommandoen:

```bash
put filnavn.txt
```

### Liste filer i katalogen
For å vise filer i den nåværende katalogen på serveren, bruk:

```bash
ls
```

### Endre katalog
For å navigere til en annen katalog på serveren, bruk:

```bash
cd katalognavn
```

## Tips
- Sørg for at du har riktige tilgangsrettigheter for å laste opp eller laste ned filer.
- Bruk `bye`-kommandoen for å avslutte FTP-økten trygt.
- Vær oppmerksom på at FTP overfører data i klartekst, så vurder å bruke SFTP for sikker overføring.