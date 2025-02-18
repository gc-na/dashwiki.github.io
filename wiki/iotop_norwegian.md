# [Norsk] Debian Almquist Shell (dash) iotop bruksområde: overvåke disk I/O

## Oversikt
`iotop` er et verktøy som brukes til å overvåke disk I/O (input/output) i sanntid. Det viser hvilke prosesser som bruker mest diskressurser, noe som kan være nyttig for feilsøking og ytelsesoptimalisering.

## Bruk
Grunnleggende syntaks for `iotop` er som følger:

```bash
iotop [alternativer] [argumenter]
```

## Vanlige alternativer
- `-o` eller `--only`: Vis kun prosesser som bruker I/O.
- `-b` eller `--batch`: Kjør i batch-modus, nyttig for logging.
- `-d <sekunder>`: Angi oppdateringsintervall i sekunder.
- `-p <PID>`: Vis I/O for en spesifikk prosess ID.

## Vanlige eksempler
For å starte `iotop` og se sanntids I/O-aktivitet, kan du bruke:

```bash
iotop
```

For å vise kun prosesser som bruker I/O, kan du bruke:

```bash
iotop -o
```

For å kjøre `iotop` i batch-modus og oppdatere hvert 5. sekund, kan du bruke:

```bash
iotop -b -d 5
```

For å overvåke I/O for en spesifikk prosess med PID 1234, kan du bruke:

```bash
iotop -p 1234
```

## Tips
- Kjør `iotop` med root-rettigheter for å få full oversikt over alle prosesser.
- Bruk `-b` alternativet hvis du ønsker å logge utdataene til en fil for senere analyse.
- Vær oppmerksom på at `iotop` kan påvirke systemytelsen, spesielt på systemer med høy I/O-aktivitet.