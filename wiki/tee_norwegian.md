# [Norsk] Debian Almquist Shell (dash) tee bruken: Kopierer standardutgang til filer

## Oversikt
`tee`-kommandoen brukes til å lese fra standard inngang og skrive til både standard utgang og en eller flere filer. Dette gjør det mulig å se utdataene på skjermen samtidig som de lagres i filene.

## Bruk
Grunnleggende syntaks for `tee`-kommandoen er som følger:

```bash
tee [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`, `--append`: Legger til utdataene til slutten av filen i stedet for å overskrive den.
- `-i`, `--ignore-interrupts`: Ignorerer signaler for avbrudd.
- `-p`, `--output-error`: Bestemmer hvordan feil ved skriving til filene skal håndteres.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `tee`:

1. **Skrive utdata til en fil og vise dem på skjermen:**

   ```bash
   echo "Hei, verden!" | tee fil.txt
   ```

2. **Legge til utdata til en eksisterende fil:**

   ```bash
   echo "Ny linje" | tee -a fil.txt
   ```

3. **Skrive utdata til flere filer samtidig:**

   ```bash
   echo "Data til flere filer" | tee fil1.txt fil2.txt
   ```

4. **Bruke tee med en annen kommando:**

   ```bash
   ls -l | tee liste.txt
   ```

## Tips
- Bruk `-a`-alternativet hvis du ønsker å bevare eksisterende innhold i filen.
- Kombiner `tee` med andre kommandoer i en pipeline for å fange utdata samtidig som du viser dem.
- Vær oppmerksom på filrettigheter; du må ha skrivetilgang til filene du prøver å skrive til.