# [Norsk] Debian Almquist Shell (dash) getopts bruksanvisning: Håndtering av kommandolinjealternativer

## Oversikt
`getopts` er et innebygd kommando i dash som brukes til å analysere kommandolinjealternativer. Det gjør det enklere å håndtere flagg og argumenter i skript, slik at brukeren kan spesifisere innstillinger og valg når de kjører skriptet.

## Bruk
Den grunnleggende syntaksen for `getopts` er som følger:

```sh
getopts [options] [arguments]
```

## Vanlige alternativer
- `-a`: Aktiverer spesifikke alternativer.
- `-b`: Brukes for å spesifisere en annen oppførsel.
- `-c`: Kan brukes for å angi en konfigurasjonsfil.
- `-d`: Aktiverer debug-modus for mer detaljert utdata.

## Vanlige eksempler

### Eksempel 1: Enkelt alternativ
Her er et enkelt skript som bruker `getopts` for å håndtere et alternativ:

```sh
#!/bin/dash

while getopts "a:" opt; do
  case $opt in
    a) echo "Alternativ A er valgt med verdi: $OPTARG" ;;
    *) echo "Ugyldig alternativ" ;;
  esac
done
```

### Eksempel 2: Flere alternativer
Dette eksemplet viser hvordan man kan håndtere flere alternativer:

```sh
#!/bin/dash

while getopts "ab:c:" opt; do
  case $opt in
    a) echo "Alternativ A er valgt" ;;
    b) echo "Alternativ B er valgt med verdi: $OPTARG" ;;
    c) echo "Alternativ C er valgt med verdi: $OPTARG" ;;
    *) echo "Ugyldig alternativ" ;;
  esac
done
```

### Eksempel 3: Bruk av debug-modus
Her er et skript som aktiverer debug-modus:

```sh
#!/bin/dash

DEBUG=0

while getopts "d" opt; do
  case $opt in
    d) DEBUG=1 ;;
    *) echo "Ugyldig alternativ" ;;
  esac
done

if [ $DEBUG -eq 1 ]; then
  echo "Debug-modus aktivert"
fi
```

## Tips
- Sørg for å bruke `OPTARG` for å hente verdien av argumentene som følger med alternativene.
- Husk å håndtere ugyldige alternativer for å gi brukeren tilbakemelding.
- Test skriptene dine med forskjellige kombinasjoner av alternativer for å sikre at de fungerer som forventet.