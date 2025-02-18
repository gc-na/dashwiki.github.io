# [Svenska] Debian Almquist Shell (dash) df användning: Visa diskutrymme

## Översikt
Kommandot `df` används för att visa information om diskutrymme som används och tillgängligt på filsystemet. Det ger en översikt över hur mycket utrymme som är upptaget och hur mycket som är ledigt på olika monterade filsystem.

## Användning
Den grundläggande syntaxen för kommandot `df` är:

```bash
df [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Visar storlekar i ett läsbart format (t.ex. MB, GB).
- `-T`: Visar typ av filsystem.
- `-a`: Inkluderar alla filsystem, även de som är 0-byte.
- `-i`: Visar information om inoder istället för diskutrymme.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `df`:

1. Visa diskutrymme i ett läsbart format:
   ```bash
   df -h
   ```

2. Visa diskutrymme med typ av filsystem:
   ```bash
   df -T
   ```

3. Visa information om alla filsystem, inklusive tomma:
   ```bash
   df -a
   ```

4. Visa information om inoder:
   ```bash
   df -i
   ```

## Tips
- Använd `df -h` för att snabbt få en översikt över diskutrymmet i ett format som är lätt att förstå.
- Kombinera alternativ för att få mer detaljerad information, till exempel `df -hT` för att se både storlek och typ av filsystem.
- Kontrollera diskutrymmet regelbundet för att undvika att fylla upp disken, vilket kan leda till systemproblem.