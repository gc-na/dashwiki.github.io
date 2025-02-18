# [Norsk] Debian Almquist Shell (dash) netstat Bruk: Vise nettverksforbindelser

## Oversikt
`netstat` er et kommandolinjeverktøy som brukes til å vise nettverksforbindelser, rutingtabeller, grensesnittstatistikk og mer. Det gir en oversikt over aktive nettverksforbindelser og kan være nyttig for feilsøking av nettverksproblemer.

## Bruk
Den grunnleggende syntaksen for `netstat` er som følger:

```bash
netstat [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-a`: Viser alle tilkoblede og lyttende porter.
- `-t`: Viser TCP-forbindelser.
- `-u`: Viser UDP-forbindelser.
- `-n`: Viser adresser og porter i numerisk format.
- `-l`: Viser bare lyttende forbindelser.
- `-p`: Viser prosess-ID og programnavn som bruker forbindelsen.

## Vanlige Eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `netstat`:

1. **Vis alle aktive forbindelser**:
   ```bash
   netstat -a
   ```

2. **Vis kun TCP-forbindelser**:
   ```bash
   netstat -t
   ```

3. **Vis lyttende porter**:
   ```bash
   netstat -l
   ```

4. **Vis forbindelser med prosessinformasjon**:
   ```bash
   netstat -p
   ```

5. **Vis forbindelser i numerisk format**:
   ```bash
   netstat -n
   ```

## Tips
- Bruk `netstat -tuln` for å få en rask oversikt over alle lyttende TCP- og UDP-porter uten å vise prosessinformasjon.
- Kombiner alternativer for å få mer spesifik informasjon, for eksempel `netstat -tunlp` for å vise både TCP og UDP med prosessinformasjon.
- Vær oppmerksom på at `netstat` kan kreve administrative rettigheter for å vise detaljer om prosesser.