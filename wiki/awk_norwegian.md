# [Norsk] Debian Almquist Shell (dash) awk Bruk: Behandle tekst og data

## Oversikt
`awk` er et kraftig tekstbehandlingsverktøy som brukes til å analysere og manipulere data i tekstfiler. Det er spesielt nyttig for å hente ut spesifikke felt fra linjer i en fil eller for å utføre beregninger basert på innholdet.

## Bruk
Den grunnleggende syntaksen for `awk` er som følger:

```bash
awk [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-F`: Angir feltseparatoren (for eksempel `-F,` for komma).
- `-v`: Setter en variabel før kjøring av programmet.
- `-f`: Leser `awk`-programmet fra en fil i stedet for fra kommandolinjen.

## Vanlige Eksempler
Her er noen praktiske eksempler på bruk av `awk`:

1. **Skrive ut det første feltet i hver linje:**
   ```bash
   awk '{print $1}' fil.txt
   ```

2. **Bruke en spesifikk feltseparator (f.eks. komma):**
   ```bash
   awk -F, '{print $2}' fil.csv
   ```

3. **Beregne summen av tall i det andre feltet:**
   ```bash
   awk '{sum += $2} END {print sum}' fil.txt
   ```

4. **Filtrere linjer der det første feltet er lik "test":**
   ```bash
   awk '$1 == "test"' fil.txt
   ```

5. **Bruke variabler til å lagre og bruke verdier:**
   ```bash
   awk -v var=10 '{print $1 + var}' fil.txt
   ```

## Tips
- Bruk `-F` for å spesifisere feltseparatoren når du arbeider med CSV-filer eller andre strukturerte data.
- Husk at `awk` starter tellingen av felt fra 1, ikke 0.
- Du kan kombinere flere `awk`-kommandoer ved å bruke semikolon for å utføre flere handlinger på én gang.