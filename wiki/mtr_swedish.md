# [Svenska] Debian Almquist Shell (dash) mtr användning: nätverksdiagnostikverktyg

## Översikt
Kommandot `mtr` (My Traceroute) kombinerar funktionerna hos `ping` och `traceroute` för att diagnostisera nätverksproblem. Det ger en realtidsvisning av nätverksvägen till en destination och mäter fördröjning och paketförlust längs vägen.

## Användning
Den grundläggande syntaxen för kommandot `mtr` är:

```
mtr [alternativ] [argument]
```

## Vanliga alternativ
- `-r`: Utför en rapportering och avsluta efter att ha skickat ett visst antal paket.
- `-c <antal>`: Anger hur många paket som ska skickas.
- `-i <intervall>`: Anger intervallet mellan paketen i sekunder.
- `-p`: Visar en portnummer för varje hopp.
- `-w`: Använd en "wide" visning för att visa mer information.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mtr`:

1. Grundläggande användning för att spåra en värd:
   ```bash
   mtr example.com
   ```

2. Utför en rapportering och avsluta efter att ha skickat 10 paket:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Ange ett intervall på 1 sekund mellan paketen:
   ```bash
   mtr -i 1 example.com
   ```

4. Visa portnummer för varje hopp:
   ```bash
   mtr -p example.com
   ```

5. Använd "wide" visning för mer detaljerad information:
   ```bash
   mtr -w example.com
   ```

## Tips
- Använd `mtr` med `sudo` om du vill ha mer detaljerad information om nätverksvägar.
- Kombinera `mtr` med andra kommandon som `grep` för att filtrera ut specifika resultat.
- Kontrollera nätverksproblem genom att köra `mtr` mot både interna och externa adresser för att isolera problemet.