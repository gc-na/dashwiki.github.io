# [Svenska] Debian Almquist Shell (dash) tee användning: [skriver ut till flera destinationer]

## Översikt
Kommandot `tee` används för att läsa från standardinmatning och skriva till både standardutmatning och en eller flera filer. Det är användbart för att duplicera dataflöden, vilket gör det möjligt att se utdata på skärmen samtidigt som den sparas i en fil.

## Användning
Den grundläggande syntaxen för kommandot är:

```
tee [alternativ] [argument]
```

## Vanliga alternativ
- `-a`, `--append`: Lägg till utdata till slutet av filen istället för att skriva över den.
- `-i`, `--ignore-interrupts`: Ignorera avbrottssignaler.
- `--help`: Visa hjälpmeddelande för `tee`.
- `--version`: Visa versionsinformation för `tee`.

## Vanliga exempel
Här är några praktiska exempel på hur `tee` kan användas:

1. Skriva ut utdata till en fil och visa på skärmen:
   ```sh
   echo "Detta är ett test" | tee fil.txt
   ```

2. Lägga till utdata till en befintlig fil:
   ```sh
   echo "Ytterligare text" | tee -a fil.txt
   ```

3. Använda `tee` med flera filer:
   ```sh
   echo "Spara detta i flera filer" | tee fil1.txt fil2.txt
   ```

4. Kombinera `tee` med andra kommandon:
   ```sh
   ls -l | tee fil.txt | grep ".txt"
   ```

## Tips
- Använd `-a` alternativet om du vill lägga till data till en fil utan att radera befintligt innehåll.
- Tänk på att `tee` kommer att skriva ut all data till standardutmatning, så om du bara vill spara till en fil utan att visa det på skärmen, kan du använda omdirigering istället.
- `tee` är särskilt användbart i skript där du vill logga utdata för senare granskning.