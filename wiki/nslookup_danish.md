# [Danish] Debian Almquist Shell (dash) nslookup brug: Forespørgsel af DNS-oplysninger

## Oversigt
`nslookup` er et kommandolinjeværktøj, der bruges til at forespørge Domain Name System (DNS) for at få oplysninger om domæner og IP-adresser. Det kan hjælpe med at diagnosticere netværksproblemer ved at give information om, hvordan domæner oversættes til IP-adresser.

## Brug
Den grundlæggende syntaks for `nslookup`-kommandoen er:

```bash
nslookup [muligheder] [argumenter]
```

## Almindelige muligheder
- `-type=TYPE`: Angiver hvilken type DNS-oplysninger, der skal forespørges, f.eks. A, MX, CNAME.
- `-timeout=sekunder`: Sætter timeout for forespørgslen.
- `-retry=antal`: Angiver antallet af forsøg ved timeout.
- `server`: Angiver en specifik DNS-server til at sende forespørgslen til.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `nslookup`:

1. Forespørgsel om en A-post for et domæne:
   ```bash
   nslookup example.com
   ```

2. Forespørgsel om MX-poster for et domæne:
   ```bash
   nslookup -type=MX example.com
   ```

3. Forespørgsel til en specifik DNS-server:
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. Forespørgsel om CNAME-poster:
   ```bash
   nslookup -type=CNAME www.example.com
   ```

## Tips
- Brug `nslookup` med en specifik DNS-server for at få mere præcise resultater, især hvis du har mistanke om problemer med din lokale DNS.
- Tjek altid både A- og CNAME-poster for at få et komplet billede af, hvordan et domæne er konfigureret.
- Hvis du arbejder med e-mail, kan det være nyttigt at kontrollere MX-poster for at sikre, at e-mailen dirigeres korrekt.