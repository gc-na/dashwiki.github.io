# [Svenska] Debian Almquist Shell (dash) dstat användning: övervaka systemresurser

## Översikt
Dstat är ett kraftfullt verktyg för att övervaka och visa systemresurser i realtid. Det kombinerar funktioner från flera andra verktyg, vilket gör det möjligt att se olika systemstatistik som CPU-användning, minnesanvändning, diskaktivitet och nätverksanvändning på ett och samma ställe.

## Användning
Den grundläggande syntaxen för dstat är:

```bash
dstat [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Visa CPU-användning.
- `-d`: Visa diskaktivitet.
- `-n`: Visa nätverksanvändning.
- `-m`: Visa minnesanvändning.
- `--time`: Visa tidsstämplar för varje rad.
- `-p`: Visa processinformation.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda dstat:

1. Visa CPU- och minnesanvändning:
   ```bash
   dstat -c -m
   ```

2. Visa disk- och nätverksaktivitet:
   ```bash
   dstat -d -n
   ```

3. Visa all systemstatistik med tidsstämplar:
   ```bash
   dstat --time -cdmn
   ```

4. Visa processinformation tillsammans med systemstatistik:
   ```bash
   dstat -p
   ```

## Tips
- Använd dstat i kombination med andra verktyg som `grep` för att filtrera specifik information.
- För långvarig övervakning, överväg att köra dstat i bakgrunden och spara utdata till en fil för senare analys.
- Experimentera med olika alternativ för att anpassa visningen efter dina behov och få en bättre översikt över systemets prestanda.