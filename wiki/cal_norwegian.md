# [Norsk] Debian Almquist Shell (dash) cal Bruk: Vise kalender

## Oversikt
`cal`-kommandoen brukes til å vise en kalender i terminalen. Den kan vise den nåværende måneden, en spesifisert måned, eller til og med en hel årskalender. Dette er nyttig for raskt å sjekke datoer uten å måtte åpne en grafisk kalenderapplikasjon.

## Bruk
Grunnleggende syntaks for `cal`-kommandoen er som følger:

```bash
cal [alternativer] [argumenter]
```

## Vanlige alternativer
- `-m`: Vis måneden i en mer kompakt form.
- `-y`: Vis hele kalenderen for inneværende år.
- `-3`: Vis kalenderen for den nåværende måneden, samt måneden før og etter.
- `-j`: Vis kalenderen med julian datoer.

## Vanlige eksempler
For å vise kalenderen for den nåværende måneden:

```bash
cal
```

For å vise kalenderen for en spesifikk måned og år (f.eks. mars 2023):

```bash
cal 03 2023
```

For å vise hele kalenderen for inneværende år:

```bash
cal -y
```

For å vise kalenderen for den nåværende måneden samt måneden før og etter:

```bash
cal -3
```

For å vise kalenderen med julian datoer:

```bash
cal -j
```

## Tips
- Bruk `cal -y` for raskt å få oversikt over hele året, noe som kan være nyttig for planlegging.
- Kombiner `cal` med andre kommandoer, som `grep`, for å finne spesifikke datoer eller hendelser.
- Husk at `cal` kan tilpasses med forskjellige alternativer for å vise akkurat det du trenger.