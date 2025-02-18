# [Svenska] Debian Almquist Shell (dash) head användning: visa de första raderna i en fil

## Översikt
`head`-kommandot används för att visa de första raderna i en fil. Det är ett enkelt och effektivt verktyg för att snabbt granska innehållet i en fil utan att behöva öppna hela filen.

## Användning
Den grundläggande syntaxen för `head`-kommandot är:

```bash
head [alternativ] [argument]
```

## Vanliga alternativ
- `-n [antal]`: Anger antalet rader som ska visas. Om inget antal anges, visas som standard de första 10 raderna.
- `-c [antal]`: Visar de första [antal] byte av filen istället för rader.
- `-q`: Tystar utdata av filnamn när flera filer anges.
- `-v`: Visar alltid filnamnet innan innehållet, även om endast en fil anges.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `head`:

1. Visa de första 10 raderna i en fil:
   ```bash
   head fil.txt
   ```

2. Visa de första 5 raderna i en fil:
   ```bash
   head -n 5 fil.txt
   ```

3. Visa de första 20 byte av en fil:
   ```bash
   head -c 20 fil.txt
   ```

4. Visa de första 10 raderna från flera filer:
   ```bash
   head fil1.txt fil2.txt
   ```

5. Visa de första 10 raderna och inkludera filnamnet:
   ```bash
   head -v fil.txt
   ```

## Tips
- Använd `head` tillsammans med andra kommandon i en pipeline för att snabbt inspektera utdata. Till exempel:
  ```bash
  ls -l | head
  ```
- För att snabbt se en del av en stor loggfil, kan du använda `head` för att få en översikt över de första raderna.
- Kombinera `head` med `tail` för att se både början och slutet av en fil.