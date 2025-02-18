# [Norsk] Debian Almquist Shell (dash) export bruk: Setter miljøvariabler

## Oversikt
`export`-kommandoen brukes i Debian Almquist Shell (dash) for å sette miljøvariabler, slik at de blir tilgjengelige for alle underprosesser som startes fra den nåværende shell-økten. Dette er nyttig for å dele konfigurasjonsinnstillinger og andre verdier mellom forskjellige programmer.

## Bruk
Den grunnleggende syntaksen for `export`-kommandoen er som følger:

```sh
export [alternativer] [argumenter]
```

## Vanlige alternativer
- `-n`: Fjerner eksporten av en variabel, slik at den ikke lenger er tilgjengelig for underprosesser.
- `-p`: Viser alle eksporterte variabler og deres verdier.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `export` kan brukes:

1. **Sette en ny miljøvariabel:**
   ```sh
   export MY_VAR="Hei, verden!"
   ```

2. **Sjekke verdien av en eksportert variabel:**
   ```sh
   echo $MY_VAR
   ```

3. **Fjerne eksporten av en variabel:**
   ```sh
   export -n MY_VAR
   ```

4. **Vise alle eksporterte variabler:**
   ```sh
   export -p
   ```

## Tips
- Husk at miljøvariabler er case-sensitive. `MY_VAR` og `my_var` vil bli behandlet som to forskjellige variabler.
- For å gjøre en variabel tilgjengelig i en annen shell-økt, kan du legge til `export`-kommandoen i din `.profile` eller `.bashrc`-fil.
- Bruk `unset`-kommandoen for å fjerne en variabel helt, ikke bare eksporten:
  ```sh
  unset MY_VAR
  ```