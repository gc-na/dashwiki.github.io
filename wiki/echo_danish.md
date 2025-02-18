# [Danish] Debian Almquist Shell (dash) echo brug: Udskriver tekst til standard output

## Oversigt
`echo`-kommandoen bruges til at udskrive tekst eller variabler til standard output (typisk terminalen). Det er en simpel, men nyttig kommando til at vise information eller til at teste skripter.

## Brug
Den grundlæggende syntaks for `echo`-kommandoen er:

```sh
echo [muligheder] [argumenter]
```

## Almindelige muligheder
- `-n`: Undlad at tilføje en ny linje efter udskrift.
- `-e`: Aktivér fortolkning af escape-sekvenser (som `\n` for ny linje).
- `-E`: Deaktiver fortolkning af escape-sekvenser (standardadfærd).

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `echo`:

1. Udskriv en simpel tekst:
   ```sh
   echo "Hej, verden!"
   ```

2. Udskriv tekst uden ny linje:
   ```sh
   echo -n "Dette er på samme linje."
   ```

3. Brug af escape-sekvenser:
   ```sh
   echo -e "Første linje\nAnden linje"
   ```

4. Udskriv værdien af en variabel:
   ```sh
   navn="Alice"
   echo "Mit navn er $navn."
   ```

## Tips
- Brug `-n` for at undgå en ny linje, når du ønsker at fortsætte på samme linje.
- Når du bruger `-e`, vær opmærksom på, at ikke alle versioner af `echo` understøtter det, så test det først.
- For at sikre, at din tekst vises korrekt, kan det være en god idé at indkapsle tekst i anførselstegn, især hvis den indeholder mellemrum eller specialtegn.