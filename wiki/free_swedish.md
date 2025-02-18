# [Svenska] Debian Almquist Shell (dash) free: Visa minnesanvändning

## Översikt
Kommandot `free` används för att visa information om systemets minnesanvändning. Det ger en översikt över det totala, använda och lediga minnet, samt buffertar och cache.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
free [alternativ]
```

## Vanliga alternativ
- `-h`: Visar minnesinformation i ett lättläst format (t.ex. MB eller GB).
- `-m`: Visar minnesinformation i megabyte.
- `-g`: Visar minnesinformation i gigabyte.
- `-s [sekunder]`: Uppdaterar och visar minnesinformation med angiven intervall i sekunder.
- `-t`: Visar en totalrad för minnesanvändning.

## Vanliga exempel
Här är några praktiska exempel på hur man använder kommandot `free`:

1. Visa minnesanvändning i standardformat:
   ```bash
   free
   ```

2. Visa minnesanvändning i ett lättläst format:
   ```bash
   free -h
   ```

3. Visa minnesanvändning i megabyte:
   ```bash
   free -m
   ```

4. Visa minnesanvändning i gigabyte:
   ```bash
   free -g
   ```

5. Visa minnesanvändning och uppdatera var 5:e sekund:
   ```bash
   free -s 5
   ```

6. Visa total minnesanvändning:
   ```bash
   free -t
   ```

## Tips
- Använd `-h` alternativet för att snabbt få en översikt över minnesanvändningen i ett mer förståeligt format.
- Kombinera `free` med andra kommandon som `watch` för att kontinuerligt övervaka minnesanvändningen:
  ```bash
  watch free -h
  ```
- Kontrollera minnesanvändning regelbundet för att identifiera eventuella problem med resursanvändning på systemet.