# [Norsk] Debian Almquist Shell (dash) dirname Bruk: Hent ut katalognavn fra stier

## Oversikt
`dirname`-kommandoen brukes til å hente ut katalognavnet fra en gitt filbane. Dette er nyttig når du ønsker å isolere katalogdelen av en sti, for eksempel når du jobber med filbehandling i skript.

## Bruk
Den grunnleggende syntaksen for `dirname`-kommandoen er som følger:

```bash
dirname [alternativer] [argumenter]
```

## Vanlige alternativer
- `-z`: Behandler stier som nullterminerte strenger.
- `--help`: Viser hjelp og informasjon om bruken av kommandoen.
- `--version`: Viser versjonsinformasjon om `dirname`.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `dirname` kan brukes:

1. Hente katalognavnet fra en filbane:
   ```bash
   dirname /home/bruker/dokumenter/fil.txt
   ```
   Utdata: `/home/bruker/dokumenter`

2. Hente katalognavnet fra en relativ sti:
   ```bash
   dirname ./bilder/foto.jpg
   ```
   Utdata: `./bilder`

3. Bruke `dirname` i et skript for å lagre katalognavnet i en variabel:
   ```bash
   STI="/var/log/syslog"
   KATALOG=$(dirname "$STI")
   echo "Katalogen er: $KATALOG"
   ```
   Utdata: `Katalogen er: /var/log`

## Tips
- Når du bruker `dirname`, vær oppmerksom på at den alltid returnerer katalogen, selv om stien slutter med en skråstrek.
- Du kan bruke `dirname` i kombinasjon med andre kommandoer, som `find`, for å organisere filer basert på deres kataloger.
- Husk å bruke anførselstegn rundt stier som inneholder mellomrom for å unngå feil i kommandoen.