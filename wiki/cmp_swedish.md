# [Svenska] Debian Almquist Shell (dash) cmp användning: Jämför filer byte för byte

## Översikt
`cmp` är ett kommandoradsverktyg som används för att jämföra två filer byte för byte. Det rapporterar den första skillnaden mellan filerna, vilket gör det användbart för att identifiera skillnader i innehåll.

## Användning
Den grundläggande syntaxen för `cmp` är:

```bash
cmp [alternativ] [fil1] [fil2]
```

## Vanliga alternativ
- `-l`: Lista alla skillnader byte för byte.
- `-s`: Tyst läge; ingen utdata, men returnerar en statuskod som indikerar om filerna är lika eller olika.
- `-i OFFSET`: Hoppa över ett visst antal byte innan jämförelsen börjar.
- `-n NUM`: Jämför endast de första NUM byte av filerna.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `cmp`:

1. Jämför två filer och visa den första skillnaden:
   ```bash
   cmp fil1.txt fil2.txt
   ```

2. Jämför två filer utan att visa utdata, bara statuskod:
   ```bash
   cmp -s fil1.txt fil2.txt
   ```

3. Lista alla skillnader mellan två filer:
   ```bash
   cmp -l fil1.txt fil2.txt
   ```

4. Jämför endast de första 10 byte av två filer:
   ```bash
   cmp -n 10 fil1.txt fil2.txt
   ```

5. Hoppa över de första 5 byte innan jämförelsen:
   ```bash
   cmp -i 5 fil1.txt fil2.txt
   ```

## Tips
- Använd `-s` alternativet för att snabbt kontrollera om två filer är lika utan att få detaljerad utdata.
- För att få en mer detaljerad översikt över skillnader, använd `-l` alternativet.
- Kom ihåg att `cmp` är känslig för filtyp; det fungerar bäst med binära och textfiler.