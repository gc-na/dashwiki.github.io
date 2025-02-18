# [Svenska] Debian Almquist Shell (dash) top användning: Visa systemprocesser i realtid

## Översikt
Kommandot `top` används för att visa en dynamisk, realtidsöversikt av systemets processer. Det ger användaren information om vilka processer som körs, hur mycket CPU och minne de använder, samt andra viktiga systemresurser.

## Användning
Den grundläggande syntaxen för `top` är:

```
top [alternativ] [argument]
```

## Vanliga alternativ
- `-d <sekunder>`: Ställer in uppdateringsintervallet för visningen i sekunder.
- `-n <antal>`: Anger hur många gånger `top` ska uppdatera visningen innan den avslutas.
- `-b`: Kör `top` i batch-läge, vilket är användbart för att skicka utdata till en fil.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `top`:

1. Starta `top` med standardinställningar:
   ```bash
   top
   ```

2. Ställ in uppdateringsintervallet till 2 sekunder:
   ```bash
   top -d 2
   ```

3. Kör `top` i batch-läge och spara utdata till en fil:
   ```bash
   top -b -n 1 > top_output.txt
   ```

4. Visa processer sorterade efter minnesanvändning:
   Inom `top`, tryck på `M` för att sortera efter minnesanvändning.

## Tips
- Använd `q` för att avsluta `top` när du är klar.
- Tryck på `h` inom `top` för att få hjälp med kommandon och kortkommandon.
- För att se specifika processer kan du använda `grep` i kombination med `top` i batch-läge:
  ```bash
  top -b -n 1 | grep <processnamn>
  ```