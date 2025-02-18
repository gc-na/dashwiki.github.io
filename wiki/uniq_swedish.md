# [Svenska] Debian Almquist Shell (dash) uniq användning: Ta bort dubbletter från en fil

## Översikt
Kommandot `uniq` används för att ta bort dubbletter från en sorterad lista med rader. Det fungerar genom att jämföra varje rad med den föregående och endast skriver ut unika rader.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
uniq [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Räkna antalet gånger varje rad förekommer.
- `-d`: Visa endast rader som förekommer mer än en gång.
- `-u`: Visa endast rader som förekommer en gång.
- `-i`: Ignorera skillnader i versaler och gemener.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `uniq`:

1. Ta bort dubbletter från en sorterad fil:
   ```bash
   uniq fil.txt
   ```

2. Räkna antalet förekomster av varje rad:
   ```bash
   uniq -c fil.txt
   ```

3. Visa endast rader som förekommer mer än en gång:
   ```bash
   uniq -d fil.txt
   ```

4. Visa endast unika rader:
   ```bash
   uniq -u fil.txt
   ```

5. Ignorera versaler och gemener:
   ```bash
   uniq -i fil.txt
   ```

## Tips
- Se till att filen är sorterad innan du använder `uniq`, annars kommer dubbletter som inte är intill varandra inte att tas bort.
- Du kan kombinera `uniq` med andra kommandon, som `sort`, för att först sortera data:
  ```bash
  sort fil.txt | uniq
  ```
- Använd `-c` alternativet för att snabbt få en översikt över hur många gånger varje rad förekommer, vilket kan vara användbart för analys.