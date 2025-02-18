# [Norsk] Debian Almquist Shell (dash) who: viser innloggede brukere

## Oversikt
`who`-kommandoen brukes til å vise en liste over brukere som for øyeblikket er innlogget på systemet. Den gir informasjon om brukernavn, terminal, innloggingsdato og -tid, samt hvor brukeren er logget inn fra.

## Bruk
Grunnleggende syntaks for `who`-kommandoen er som følger:

```
who [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser all tilgjengelig informasjon, inkludert innloggings- og utloggingshistorikk.
- `-b`: Viser tidspunktet for siste systemoppstart.
- `-q`: Viser bare antall innloggede brukere og deres brukernavn.
- `--help`: Viser hjelp og tilgjengelige alternativer for kommandoen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `who` kan brukes:

1. **Vis alle innloggede brukere:**
   ```bash
   who
   ```

2. **Vis detaljert informasjon om innloggede brukere:**
   ```bash
   who -a
   ```

3. **Vis tidspunktet for siste systemoppstart:**
   ```bash
   who -b
   ```

4. **Vis bare antall innloggede brukere:**
   ```bash
   who -q
   ```

## Tips
- Bruk `who` sammen med `grep` for å filtrere spesifikke brukere:
  ```bash
  who | grep brukernavn
  ```
- Kombiner `who` med `wc -l` for å telle antall innloggede brukere:
  ```bash
  who | wc -l
  ```
- For mer informasjon om en spesifikk bruker, kan du bruke `finger`-kommandoen hvis den er installert:
  ```bash
  finger brukernavn
  ```