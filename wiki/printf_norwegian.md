# [Norsk] Debian Almquist Shell (dash) printf Bruk: Formatert utskrift av tekst

## Oversikt
`printf`-kommandoen brukes til å formatere og skrive ut tekst til standard utgang. Den gir mer kontroll over formatet enn den enklere `echo`-kommandoen, noe som gjør den nyttig for skripting og programmering.

## Bruk
Grunnleggende syntaks for `printf`-kommandoen er:

```sh
printf [alternativer] [argumenter]
```

## Vanlige alternativer
- `-v VAR`: Lagre resultatet i en variabel i stedet for å skrive det ut.
- `--help`: Vis hjelpemelding med tilgjengelige alternativer.
- `--version`: Vis versjonsinformasjon for `printf`.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `printf` kan brukes:

### Eksempel 1: Enkel tekstutskrift
```sh
printf "Hei, verden!\n"
```

### Eksempel 2: Formatert tallutskrift
```sh
printf "Tallet er: %.2f\n" 3.14159
```

### Eksempel 3: Utskrift med flere argumenter
```sh
printf "Navn: %s, Alder: %d\n" "Ola" 30
```

### Eksempel 4: Utskrift til en variabel
```sh
printf -v result "Resultatet er: %.1f" 42.5
echo "$result"
```

## Tips
- Bruk `\n` for å legge til linjeskift i utskriften.
- For å formatere tall, kan du bruke spesifikatorer som `%d` for heltall og `%f` for desimaltall.
- Husk at `printf` ikke automatisk legger til linjeskift, så du må spesifisere det selv hvis nødvendig.