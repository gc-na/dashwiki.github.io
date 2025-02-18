# [Svenska] Debian Almquist Shell (dash) bg användning: Skicka en process till bakgrunden

## Översikt
Kommandot `bg` används för att återuppta en pausad process och köra den i bakgrunden. Detta är användbart när du vill frigöra terminalen för andra kommandon medan en process fortsätter att köras.

## Användning
Den grundläggande syntaxen för `bg` är:

```bash
bg [jobbnummer]
```

## Vanliga alternativ
- **jobbnummer**: Anger vilket jobb som ska köras i bakgrunden. Om inget jobbnummer anges, används det senaste pausade jobbet.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `bg`:

1. **Skicka det senaste pausade jobbet till bakgrunden**:
   ```bash
   bg
   ```

2. **Skicka ett specifikt jobb till bakgrunden** (antag att jobbnummer 1 är pausat):
   ```bash
   bg %1
   ```

3. **Kombinera med `jobs` för att se aktiva jobb**:
   ```bash
   jobs
   bg %2
   ```

## Tips
- Använd `jobs`-kommandot för att lista alla aktiva och pausade jobb innan du använder `bg`.
- Om du vill återuppta ett jobb i förgrunden istället för i bakgrunden, använd kommandot `fg` istället.
- Kom ihåg att bakgrundsprocesser kan skriva ut till terminalen, vilket kan göra det svårt att följa med i vad som händer.