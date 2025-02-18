# [Svenska] Debian Almquist Shell (dash) comm kommando: Jämför två sorterade filer

## Översikt
Kommando `comm` används för att jämföra två sorterade filer rad för rad. Det visar skillnader och likheter mellan dessa filer, vilket gör det enkelt att se vad som är unikt för varje fil och vad som är gemensamt.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
comm [alternativ] [fil1] [fil2]
```

## Vanliga alternativ
- `-1`: Undertrycker utdata av rader som endast finns i den första filen.
- `-2`: Undertrycker utdata av rader som endast finns i den andra filen.
- `-3`: Undertrycker utdata av rader som finns i båda filerna.
- `-i`: Ignorerar skillnader i versaler och gemener.

## Vanliga exempel
Här är några praktiska exempel på hur `comm` kan användas:

1. Jämför två filer och visa alla rader:
   ```bash
   comm fil1.txt fil2.txt
   ```

2. Visa endast rader som finns i den första filen:
   ```bash
   comm -13 fil1.txt fil2.txt
   ```

3. Visa endast rader som finns i den andra filen:
   ```bash
   comm -12 fil1.txt fil2.txt
   ```

4. Ignorera versaler och gemener när du jämför:
   ```bash
   comm -i fil1.txt fil2.txt
   ```

## Tips
- Se till att filerna är sorterade innan du använder `comm`, annars kan resultaten bli otydliga.
- Använd alternativ som `-1`, `-2`, och `-3` för att skräddarsy utdata efter dina behov.
- För att snabbt sortera filer kan du använda `sort` i kombination med `comm`, exempelvis:
  ```bash
  comm <(sort fil1.txt) <(sort fil2.txt)
  ```