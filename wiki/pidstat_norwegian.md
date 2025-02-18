# [Norsk] Debian Almquist Shell (dash) pidstat bruksanvisning: overvåke prosessytelse

## Oversikt
`pidstat` er et verktøy som brukes til å overvåke ytelsen til prosesser i sanntid. Det gir detaljerte statistikker om CPU-bruk, minnebruk og andre ressurser for spesifikke prosesser, noe som er nyttig for systemadministrasjon og feilsøking.

## Bruk
Grunnleggende syntaks for `pidstat` er som følger:

```bash
pidstat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`: Viser overskrifter for hver kolonne.
- `-r`: Viser minnebruk.
- `-u`: Viser CPU-bruk.
- `-p <PID>`: Angir prosess-ID (PID) for å overvåke en spesifikk prosess.
- `-t`: Viser tråder i prosessen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `pidstat`:

1. **Overvåke CPU-bruk for alle prosesser:**
   ```bash
   pidstat -u 1
   ```
   Dette viser CPU-bruken for alle prosesser hvert sekund.

2. **Overvåke minnebruk for en spesifikk prosess:**
   ```bash
   pidstat -r -p 1234 1
   ```
   Her overvåkes minnebruken for prosessen med PID 1234 hvert sekund.

3. **Vise informasjon om tråder i en prosess:**
   ```bash
   pidstat -t -p 5678 1
   ```
   Dette viser trådstatistikk for prosessen med PID 5678 hvert sekund.

4. **Vise overskrifter for kolonnene:**
   ```bash
   pidstat -h -u 1
   ```
   Dette viser CPU-bruken med overskrifter for kolonnene hvert sekund.

## Tips
- Bruk `pidstat` i kombinasjon med andre verktøy som `grep` for å filtrere spesifikke prosesser.
- Kjør `pidstat` med `-h` for å få en bedre forståelse av hva hver kolonne representerer.
- For langvarig overvåking, vurder å bruke `pidstat` i et skript som logger data til en fil for senere analyse.