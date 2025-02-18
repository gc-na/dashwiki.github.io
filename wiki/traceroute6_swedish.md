# [Svenska] Debian Almquist Shell (dash) traceroute6 användning: Spåra nätverksvägar för IPv6

## Översikt
Kommandot `traceroute6` används för att spåra vägen som datapaket tar genom ett IPv6-nätverk. Det hjälper användare att identifiera nätverksproblem genom att visa varje hopp mellan källan och destinationen.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
traceroute6 [alternativ] [argument]
```

## Vanliga alternativ
- `-m <max_hops>`: Anger det maximala antalet hopp som ska spåras.
- `-w <timeout>`: Ställer in tidsgränsen (i sekunder) för att vänta på svar.
- `-q <queries>`: Anger antalet förfrågningar som ska skickas till varje hopp.
- `-n`: Använd IP-adresser istället för att försöka lösa domännamn.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `traceroute6`:

1. Spåra vägen till en specifik IPv6-adress:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Spåra vägen med ett maximalt antal hopp på 15:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. Spåra vägen och visa IP-adresser utan domännamn:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

4. Spåra vägen med en tidsgräns på 2 sekunder:
   ```bash
   traceroute6 -w 2 2001:db8::1
   ```

## Tips
- Använd `-n` alternativet för att snabba upp processen om du inte behöver domännamn.
- Kontrollera att du har rätt behörigheter för att köra kommandot, eftersom vissa system kan kräva administratörsrättigheter.
- Använd `traceroute6` i kombination med andra nätverksdiagnostikverktyg som `ping` för att få en bättre förståelse av nätverksproblem.