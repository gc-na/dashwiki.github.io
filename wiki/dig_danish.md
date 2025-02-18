# [Dansk] Debian Almquist Shell (dash) dig brug: Hent DNS-oplysninger

## Oversigt
`dig` (Domain Information Groper) er et værktøj, der bruges til at forespørge DNS (Domain Name System) for at hente oplysninger om domæner. Det er nyttigt til fejlfinding af DNS-problemer og til at få detaljerede oplysninger om DNS-poster.

## Brug
Den grundlæggende syntaks for `dig`-kommandoen er:

```bash
dig [muligheder] [argumenter]
```

## Almindelige muligheder
- `@server`: Angiver en specifik DNS-server til at sende forespørgslen til.
- `-t type`: Angiver typen af DNS-post, f.eks. A, AAAA, MX, TXT osv.
- `+short`: Viser kun de mest relevante oplysninger i et kort format.
- `+trace`: Følger DNS-forespørgslerne fra rodserverne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `dig`:

1. Hent A-posten for et domæne:
   ```bash
   dig example.com A
   ```

2. Hent MX-posten for et domæne:
   ```bash
   dig example.com MX
   ```

3. Brug en specifik DNS-server:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. Få en kort oversigt over A-posten:
   ```bash
   dig example.com A +short
   ```

5. Følg DNS-forespørgsler fra rodserverne:
   ```bash
   dig example.com +trace
   ```

## Tips
- Brug `+short` for at få hurtigere og mere overskuelige resultater, når du kun har brug for grundlæggende oplysninger.
- Hvis du arbejder med flere domæner, kan du overveje at skrive et script, der automatiserer `dig`-forespørgslerne.
- Hold øje med TTL (Time to Live) værdien i resultaterne for at forstå, hvor længe oplysningerne caches.