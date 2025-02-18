# [Norsk] Debian Almquist Shell (dash) scp Bruk: Kopiere filer sikkert mellom vertsmaskiner

## Oversikt
`scp` (Secure Copy Protocol) er et kommandoverktøy som brukes til å kopiere filer og kataloger mellom vertsmaskiner over et nettverk. Det bruker SSH-protokollen for å sikre dataoverføringen, noe som gjør det til et trygt alternativ for filoverføring.

## Bruk
Den grunnleggende syntaksen for `scp`-kommandoen er som følger:

```bash
scp [alternativer] [kilde] [mål]
```

## Vanlige alternativer
- `-r`: Kopierer kataloger rekursivt.
- `-P`: Angir portnummeret for SSH-tilkoblingen.
- `-i`: Spesifiserer en privat nøkkel for autentisering.
- `-v`: Aktiverer detaljert utdata for feilsøking.

## Vanlige eksempler
Kopiere en fil fra lokal maskin til en ekstern server:

```bash
scp fil.txt bruker@server:/sti/til/mål/
```

Kopiere en fil fra en ekstern server til lokal maskin:

```bash
scp bruker@server:/sti/til/fil.txt /lokal/sti/
```

Kopiere en katalog rekursivt fra lokal maskin til ekstern server:

```bash
scp -r katalog/ bruker@server:/sti/til/mål/
```

Kopiere en fil fra en ekstern server til en annen ekstern server:

```bash
scp bruker1@server1:/sti/til/fil.txt bruker2@server2:/sti/til/mål/
```

## Tips
- Bruk `-P` for å spesifisere en annen port hvis SSH-serveren kjører på en ikke-standard port.
- Sørg for at du har de nødvendige tillatelsene for å lese fra kilden og skrive til målet.
- For store filer, vurder å bruke `rsync` for mer effektiv overføring og mulighet for gjenopptak av avbrutte overføringer.