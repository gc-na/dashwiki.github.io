# [Svenska] Debian Almquist Shell (dash) du: visa diskanvändning

## Översikt
`du` (diskanvändning) är ett kommando som används för att uppskatta och visa mängden diskutrymme som används av filer och kataloger i ett filsystem. Det är ett användbart verktyg för att övervaka och hantera diskresurser.

## Användning
Den grundläggande syntaxen för `du` är:

```
du [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Visar storlekar i ett lättläst format (t.ex. KB, MB, GB).
- `-s`: Visar endast den totala storleken för varje argument, utan att lista underkataloger.
- `-c`: Summerar storlekarna av alla angivna argument och visar en total.
- `-a`: Visar storleken för både filer och kataloger.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `du`:

1. Visa diskanvändning för den aktuella katalogen:
   ```bash
   du
   ```

2. Visa diskanvändning med lättlästa storlekar:
   ```bash
   du -h
   ```

3. Visa den totala storleken för en specifik katalog:
   ```bash
   du -sh /path/to/directory
   ```

4. Visa storleken för alla filer och kataloger i den aktuella katalogen:
   ```bash
   du -ah
   ```

5. Summera storlekarna av flera kataloger:
   ```bash
   du -ch /path/to/directory1 /path/to/directory2
   ```

## Tips
- Använd `-h` för att göra storlekar mer läsbara, särskilt när du arbetar med stora filer eller kataloger.
- Kombinera `-s` och `-c` för att snabbt få en total storlek av flera kataloger utan att se detaljerna.
- Tänk på att `du` kan ta tid att köra på mycket stora kataloger, så planera användningen av kommandot i enlighet med det.