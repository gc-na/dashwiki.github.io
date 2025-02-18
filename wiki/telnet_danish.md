# [Danish] Debian Almquist Shell (dash) telnet brug: Opret forbindelse til en fjernserver

## Oversigt
`telnet`-kommandoen bruges til at oprette en forbindelse til en fjernserver ved hjælp af Telnet-protokollen. Det giver brugerne mulighed for at kommunikere med servere og netværksenheder over et netværk.

## Brug
Den grundlæggende syntaks for `telnet`-kommandoen er som følger:

```bash
telnet [options] [arguments]
```

## Almindelige muligheder
- `-l user`: Angiver brugernavnet til login på serveren.
- `-d`: Aktiverer debug-tilstand for at vise detaljerede fejlmeddelelser.
- `-h`: Viser hjælp og tilgængelige muligheder.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `telnet`:

1. Opret forbindelse til en server på standardporten (port 23):
   ```bash
   telnet example.com
   ```

2. Opret forbindelse til en server på en specifik port (f.eks. port 80):
   ```bash
   telnet example.com 80
   ```

3. Log ind med et specifikt brugernavn:
   ```bash
   telnet -l myusername example.com
   ```

4. Aktivér debug-tilstand:
   ```bash
   telnet -d example.com
   ```

## Tips
- Brug `telnet` til at teste forbindelser til servere og porte for at sikre, at de er tilgængelige.
- Vær opmærksom på, at Telnet ikke krypterer data, så undgå at sende følsomme oplysninger.
- Overvej at bruge SSH i stedet for Telnet for en mere sikker forbindelse.