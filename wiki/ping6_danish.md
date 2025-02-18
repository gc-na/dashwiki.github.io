# [Danish] Debian Almquist Shell (dash) ping6 brug: Tester IPv6 netværksforbindelse

## Oversigt
`ping6` er et netværksdiagnosticeringsværktøj, der bruges til at teste forbindelsen til en IPv6-adresse. Det sender ICMPv6 Echo Request-pakker til den angivne adresse og venter på svar, hvilket hjælper med at identificere netværksproblemer.

## Brug
Den grundlæggende syntaks for `ping6`-kommandoen er som følger:

```bash
ping6 [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c <antal>`: Angiver antallet af pakker, der skal sendes.
- `-i <interval>`: Angiver intervallet mellem pakkerne i sekunder.
- `-w <timeout>`: Angiver en tidsgrænse for, hvor længe der skal ventes på svar.
- `-s <størrelse>`: Angiver størrelsen på de sendte pakker.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `ping6`:

1. **Ping en IPv6-adresse**:
   ```bash
   ping6 2001:db8::1
   ```

2. **Send 5 pakker til en adresse**:
   ```bash
   ping6 -c 5 2001:db8::1
   ```

3. **Angiv intervallet mellem pakkerne til 2 sekunder**:
   ```bash
   ping6 -i 2 2001:db8::1
   ```

4. **Sæt en timeout på 10 sekunder**:
   ```bash
   ping6 -w 10 2001:db8::1
   ```

5. **Send pakker med en specifik størrelse**:
   ```bash
   ping6 -s 1280 2001:db8::1
   ```

## Tips
- Brug `-c` for at begrænse antallet af pakker, så du ikke overbelaster netværket.
- Tjek din netværksforbindelse ved at pinge en kendt IPv6-adresse, som f.eks. en offentlig DNS-server.
- Overvåg svarene for at identificere eventuelle tabte pakker, hvilket kan indikere netværksproblemer.