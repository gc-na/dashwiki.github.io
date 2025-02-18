# [Norsk] Debian Almquist Shell (dash) batch bruk: Kjør kommandoer i bakgrunnen

## Oversikt
`batch`-kommandoen brukes til å planlegge oppgaver som skal kjøres i bakgrunnen når systemet er ledig. Dette er nyttig for å utføre ressurstunge oppgaver uten å forstyrre brukerens arbeid.

## Bruk
Den grunnleggende syntaksen for `batch`-kommandoen er:

```bash
batch [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f`: Spesifiserer en fil som inneholder kommandoene som skal kjøres.
- `-q`: Kjør i stille modus, uten å vise meldinger til brukeren.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `batch`:

### Kjør en enkel kommando
For å kjøre en enkel kommando som `echo`, kan du bruke:

```bash
echo "Hei, verden!" | batch
```

### Kjør flere kommandoer fra en fil
Hvis du har en fil som heter `kommandoer.txt` med flere kommandoer, kan du kjøre dem med:

```bash
batch < kommandoer.txt
```

### Bruke alternativet -f
For å spesifisere en fil med kommandoer, kan du bruke:

```bash
batch -f kommandoer.txt
```

## Tips
- Sørg for at systemet har tilstrekkelig ressurser tilgjengelig før du planlegger tunge oppgaver.
- Bruk `at`-kommandoen hvis du ønsker mer kontroll over tidspunktet for når kommandoene skal kjøres.
- Sjekk systemets kø for planlagte oppgaver med `atq` for å se hva som er planlagt.