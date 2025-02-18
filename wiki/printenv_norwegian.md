# [Norsk] Debian Almquist Shell (dash) printenv Bruk: Vise miljøvariabler

## Oversikt
`printenv`-kommandoen brukes til å vise miljøvariabler i Unix-lignende operativsystemer. Den gir en enkel måte å se hvilke variabler som er tilgjengelige i det nåværende miljøet, samt deres verdier.

## Bruk
Grunnleggende syntaks for `printenv`-kommandoen er som følger:

```sh
printenv [alternativer] [argumenter]
```

## Vanlige alternativer
- `-0`: Skiller ut variabler med nullbyte i stedet for nye linjer.
- `VARIABEL`: Hvis du spesifiserer en variabel, vil `printenv` vise verdien av den spesifikke variabelen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `printenv`:

1. Vise alle miljøvariabler:
   ```sh
   printenv
   ```

2. Vise verdien av en spesifikk variabel, for eksempel `HOME`:
   ```sh
   printenv HOME
   ```

3. Vise verdien av `PATH`-variabelen:
   ```sh
   printenv PATH
   ```

4. Vise miljøvariabler med nullbyte som skille:
   ```sh
   printenv -0
   ```

## Tips
- Bruk `printenv` sammen med `grep` for å filtrere spesifikke variabler:
  ```sh
  printenv | grep USER
  ```
- For å se alle miljøvariabler i en mer lesbar form, kan du kombinere `printenv` med `less`:
  ```sh
  printenv | less
  ```
- Husk at `printenv` kun viser miljøvariabler som er satt. Hvis en variabel ikke er definert, vil den ikke vises i utdataene.