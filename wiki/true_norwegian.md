# [Norsk] Debian Almquist Shell (dash) true bruk: Utfør alltid vellykket

## Oversikt
`true` er en enkel kommando i Debian Almquist Shell (dash) som alltid returnerer en vellykket statuskode (0). Den brukes ofte i skript og kommandolinjer for å indikere at en operasjon har lykkes, eller for å opprettholde syntaksen i situasjoner der en kommando kreves, men ingen handling er nødvendig.

## Bruk
Den grunnleggende syntaksen for `true` er:

```bash
true [alternativer] [argumenter]
```

## Vanlige alternativer
`true` har ingen spesifikke alternativer eller argumenter, da dens eneste funksjon er å returnere en vellykket statuskode.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `true` kan brukes:

### Eksempel 1: Bruke true i et skript
```bash
#!/bin/dash
if true; then
    echo "Denne blokken kjører alltid."
fi
```

### Eksempel 2: Kombinere med andre kommandoer
```bash
true && echo "Denne meldingen vises alltid."
```

### Eksempel 3: Bruke true i en while-løkke
```bash
while true; do
    echo "Dette vil fortsette å kjøre."
    sleep 1
done
```

## Tips
- `true` er nyttig i skript for å opprettholde syntaksen der en kommando kreves, men ingen spesifikke handlinger er nødvendige.
- Kombiner `true` med `&&` for å kjøre flere kommandoer sekvensielt, der den første alltid lykkes.
- Bruk `true` i løkker for å lage uendelige sløyfer, men vær forsiktig med å inkludere en måte å avslutte sløyfen på.