# [Svenska] Debian Almquist Shell (dash) pwd användning: visar den aktuella katalogen

## Översikt
Kommandot `pwd` (print working directory) används för att visa den aktuella arbetskatalogen i terminalen. Det är ett enkelt men viktigt verktyg för att navigera i filsystemet.

## Användning
Den grundläggande syntaxen för kommandot är:

```
pwd [alternativ] [argument]
```

## Vanliga alternativ
- `-L`: Visar den logiska sökvägen till den aktuella katalogen, vilket kan inkludera symboliska länkar.
- `-P`: Visar den fysiska sökvägen till den aktuella katalogen, vilket innebär att eventuella symboliska länkar löses.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `pwd`:

1. Visa den aktuella katalogen:
   ```sh
   pwd
   ```

2. Visa den logiska sökvägen:
   ```sh
   pwd -L
   ```

3. Visa den fysiska sökvägen:
   ```sh
   pwd -P
   ```

## Tips
- Använd `pwd` ofta för att bekräfta din plats i filsystemet, särskilt när du navigerar mellan olika kataloger.
- Kombinera `pwd` med andra kommandon för att skapa skript som automatiskt kan referera till den aktuella katalogen.