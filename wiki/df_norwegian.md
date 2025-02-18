# [Norsk] Debian Almquist Shell (dash) df Bruk: Vise diskplassbruk

## Oversikt
`df`-kommandoen brukes til å vise informasjon om diskplassbruk på filsystemer. Den gir en oversikt over hvor mye plass som er brukt og hvor mye som er tilgjengelig på de monterte filsystemene.

## Bruk
Grunnleggende syntaks for `df`-kommandoen er som følger:

```bash
df [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`: Viser størrelser i et lesbart format (f.eks. MB, GB).
- `-T`: Viser filsystemtype for hvert montert filsystem.
- `-a`: Viser informasjon om alle filsystemer, inkludert de som har 0 brukt plass.
- `-i`: Viser informasjon om inode-bruk i stedet for diskplass.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `df`-kommandoen:

1. Vise diskplassbruk i et lesbart format:
   ```bash
   df -h
   ```

2. Vise diskplassbruk med filsystemtype:
   ```bash
   df -T
   ```

3. Vise informasjon om alle filsystemer:
   ```bash
   df -a
   ```

4. Vise inode-bruk:
   ```bash
   df -i
   ```

## Tips
- Bruk `df -h` for å få en rask oversikt over diskplass som er lett å lese.
- Kombiner `df` med `grep` for å filtrere spesifikke filsystemer, for eksempel:
  ```bash
  df -h | grep /dev/sda1
  ```
- Sjekk diskplass regelmessig for å unngå at systemet går tom for plass, noe som kan føre til ytelsesproblemer.