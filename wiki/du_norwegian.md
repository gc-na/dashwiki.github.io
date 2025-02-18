# [Norsk] Debian Almquist Shell (dash) du: [viser diskbruk]

## Oversikt
`du` (diskbruk) er et kommandoverktøy som brukes til å vise størrelsen på filer og kataloger i et filsystem. Det gir deg en oversikt over hvor mye plass hver fil eller katalog tar opp, noe som er nyttig for å administrere diskplassen.

## Bruk
Grunnleggende syntaks for `du`-kommandoen er som følger:

```bash
du [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`: Viser størrelsen i et lesbart format (f.eks. KB, MB).
- `-s`: Viser total størrelsen for hver oppgitt katalog.
- `-c`: Gir en total oppsummering av størrelsen for alle oppgitte filer og kataloger.
- `-a`: Viser størrelsen på alle filer, ikke bare kataloger.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `du`:

1. Vise diskbruk for den nåværende katalogen:
   ```bash
   du
   ```

2. Vise diskbruk i et lesbart format:
   ```bash
   du -h
   ```

3. Vise total størrelsen for en spesifikk katalog:
   ```bash
   du -sh /sti/til/katalog
   ```

4. Vise diskbruk for alle filer og kataloger i den nåværende katalogen:
   ```bash
   du -a
   ```

5. Vise diskbruk med en total oppsummering:
   ```bash
   du -ch /sti/til/katalog/*
   ```

## Tips
- Bruk `-h` for å gjøre det lettere å lese størrelsene, spesielt når du jobber med store filer.
- Kombiner `-s` og `-c` for å få en rask oversikt over total diskbruk for flere kataloger.
- Vær oppmerksom på at `du` kan ta litt tid å kjøre i store filsystemer, så vær tålmodig.
- For å få en mer detaljert visning, kan du bruke `--max-depth=N` for å begrense hvor dypt inn i katalogstrukturen du vil gå.