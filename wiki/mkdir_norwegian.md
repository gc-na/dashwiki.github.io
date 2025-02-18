# [Norsk] Debian Almquist Shell (dash) mkdir Bruk: Opprett kataloger

## Oversikt
`mkdir`-kommandoen brukes til å opprette nye kataloger i filsystemet. Den er en enkel, men viktig del av å organisere filer og mapper på systemet ditt.

## Bruk
Grunnleggende syntaks for `mkdir`-kommandoen er som følger:

```bash
mkdir [alternativer] [argumenter]
```

## Vanlige alternativer
- `-p`: Opprett foreldrekataloger om de ikke allerede eksisterer.
- `-m`: Angi tillatelser for den nye katalogen ved opprettelse.
- `--help`: Vis hjelp og informasjon om kommandoen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `mkdir`:

1. Opprett en enkel katalog:
   ```bash
   mkdir ny_katalog
   ```

2. Opprett flere kataloger samtidig:
   ```bash
   mkdir katalog1 katalog2 katalog3
   ```

3. Opprett en katalog med foreldrekataloger:
   ```bash
   mkdir -p /sti/til/ny/katalog
   ```

4. Opprett en katalog med spesifikke tillatelser:
   ```bash
   mkdir -m 755 sikret_katalog
   ```

## Tips
- Bruk `-p` alternativet når du oppretter flere nivåer av kataloger for å unngå feil hvis foreldrekatalogene ikke eksisterer.
- Sjekk alltid tillatelsene til katalogene du oppretter for å sikre at de er i samsvar med sikkerhetskravene dine.
- Kombiner `mkdir` med andre kommandoer som `cd` for å navigere til den nye katalogen umiddelbart etter opprettelsen.