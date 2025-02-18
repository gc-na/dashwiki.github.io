# [Svenska] Debian Almquist Shell (dash) strace användning: Spåra systemanrop

## Översikt
`strace` är ett kraftfullt verktyg som används för att spåra systemanrop och signaler som ett program gör under sin körning. Det är särskilt användbart för felsökning och analys av programbeteende, vilket gör det enklare att identifiera problem eller förstå hur ett program interagerar med operativsystemet.

## Användning
Den grundläggande syntaxen för `strace` är:

```bash
strace [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Sammanställ statistik över systemanrop.
- `-e expr`: Filtrera systemanrop baserat på ett uttryck.
- `-p pid`: Spåra ett redan körande program med det angivna process-ID:t.
- `-o filnamn`: Skriv ut strace-resultatet till en fil istället för till standardutgången.
- `-f`: Följ barnprocesser som skapas av det spårade programmet.

## Vanliga exempel
Här är några praktiska exempel på hur `strace` kan användas:

1. Spåra ett program och visa dess systemanrop:
   ```bash
   strace ls
   ```

2. Skriv ut resultatet till en fil:
   ```bash
   strace -o output.txt ls
   ```

3. Spåra ett redan körande program med process-ID 1234:
   ```bash
   strace -p 1234
   ```

4. Sammanställ statistik över systemanrop:
   ```bash
   strace -c ls
   ```

5. Filtrera systemanrop för att endast visa `open` och `close`:
   ```bash
   strace -e trace=open,close ls
   ```

## Tips
- Använd `-f` om du vill se systemanrop från barnprocesser, vilket är viktigt för program som skapar nya processer.
- För att snabbt få en översikt över vilka systemanrop som görs, använd `-c` för att få en sammanställning.
- Var försiktig med att spåra program som kan generera mycket utdata, eftersom det kan bli överväldigande. Använd filtrering för att fokusera på specifika anrop.