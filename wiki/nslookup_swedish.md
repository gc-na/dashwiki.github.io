# [Svenska] Debian Almquist Shell (dash) nslookup användning: Hämta DNS-information

## Översikt
Kommandot `nslookup` används för att fråga domännamnssystemet (DNS) för att få information om domännamn och IP-adresser. Det är ett kraftfullt verktyg för att diagnostisera nätverksproblem och kontrollera DNS-poster.

## Användning
Den grundläggande syntaxen för kommandot är:

```
nslookup [alternativ] [argument]
```

## Vanliga alternativ
- `-type=TYPE`: Specificera typen av DNS-post att fråga, t.ex. A, AAAA, MX, etc.
- `-timeout=sekunder`: Ställ in timeout för frågan.
- `-retry=antal`: Ange hur många gånger att försöka fråga DNS-servern.
- `server`: Ange en specifik DNS-server att fråga.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `nslookup`:

1. Hämta IP-adressen för en domän:
   ```bash
   nslookup example.com
   ```

2. Fråga en specifik typ av post, t.ex. MX-poster:
   ```bash
   nslookup -type=MX example.com
   ```

3. Använda en specifik DNS-server:
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. Kontrollera AAAA-poster för en domän:
   ```bash
   nslookup -type=AAAA example.com
   ```

## Tips
- Använd `nslookup` för att felsöka DNS-problem genom att jämföra svar från olika DNS-servrar.
- Kontrollera alltid att du använder en pålitlig DNS-server för att få korrekta svar.
- Tänk på att `nslookup` kan ge olika resultat beroende på vilken DNS-server du frågar.