# [Norsk] Debian Almquist Shell (dash) umask bruksanvisning: Angi standard filrettigheter

## Oversikt
`umask`-kommandoen brukes til å angi standard tillatelser for nye filer og kataloger i Unix-lignende operativsystemer. Den bestemmer hvilke tillatelser som skal "maskeres" eller fjernes fra standardinnstillingene når nye filer opprettes.

## Bruk
Grunnleggende syntaks for `umask`-kommandoen er som følger:

```sh
umask [alternativer] [argumenter]
```

## Vanlige alternativer
- `-S`: Viser umask-verdien i symbolsk format.
- `-p`: Viser den nåværende umask-innstillingen i et format som kan brukes i skript.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `umask` kan brukes:

### Sjekke nåværende umask-verdi
For å se den nåværende umask-verdien, kan du bruke:

```sh
umask
```

### Angi en ny umask-verdi
For å angi en ny umask-verdi, for eksempel `022`, som gir skrivetillatelser til eieren og lesetillatelser til gruppe og andre, kan du bruke:

```sh
umask 022
```

### Vise umask i symbolsk format
For å vise den nåværende umask-innstillingen i symbolsk format, kan du bruke:

```sh
umask -S
```

### Angi umask for en spesifikk sesjon
For å angi umask for en spesifikk sesjon, kan du bruke:

```sh
umask 077
# Opprett en ny fil
touch ny_fil.txt
```

## Tips
- Husk at umask-verdien er en maske, så lavere verdier gir flere tillatelser. For eksempel, en umask på `000` gir full tilgang til alle.
- Det kan være nyttig å sette umask-verdien i startskriptene dine (som `.bashrc` eller `.profile`) for å sikre at den alltid er i ønsket tilstand når du logger inn.
- Vær oppmerksom på at umask-innstillingen bare påvirker nye filer og kataloger, ikke eksisterende.